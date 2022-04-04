# Flutter-Helper
————————————————————————————————————————————————————————————————————————
Rich Text:-
————————————————————————————————————————————————————————————————————————

Container(
  margin: EdgeInsets.only(top: size.height * 0.02),
  child: RichText(
      text: TextSpan(children: [
    TextSpan(
        text: "Rate",
        style: textTheme.headline6.copyWith(
            color: themeColor.primaryColor)),
    TextSpan(
        text: " Buyer", style: textTheme.headline6),
  ])),
),
————————————————————————————————————————————————————————————————————————
Cached Network Image (Round Image)
————————————————————————————————————————————————————————————————————————
CachedNetworkImage(
  imageUrl: Constant.STORAGE_PATH +
      jobDetail['consumer_avatar'],
  imageBuilder: (context, imageProvider) =>
      Container(
    width: size.width * 0.15,
    height: size.width * 0.15,
    decoration: BoxDecoration(
      shape: BoxShape.circle,
      image: DecorationImage(
          image: imageProvider,
          fit: BoxFit.cover),
    ),
  ),
  placeholder: (context, url) => Center(
    child: SizedBox(
      width: 40.0,
      height: 40.0,
      child: new CircularProgressIndicator(),
    ),
  ),
  errorWidget: (context, url, error) =>
      Image.asset(
    "assets/icons/app-icon.png",
    width: size.width * 0.15,
    height: size.width * 0.15,
    fit: BoxFit.contain,
  ),
),
————————————————————————————————————————————————————————————————————————————————————————————————————————————————————————————————————————————————
Firebase Date time convert:- (Ex:-Timestamp(seconds=1645856985, nanoseconds=821000000))
————————————————————————————————————————————————————————————————————————————————————————————————————————————————————————————————————————————————

print(DateFormat.yMd().format(
    DateTime.fromMicrosecondsSinceEpoch(firedata[0]
            ['start_time']
        .microsecondsSinceEpoch)));

OUTPUT:-  2/26/2022


print(DateFormat.jm().format(
    DateTime.fromMicrosecondsSinceEpoch(firedata[0]
            ['start_time']
        .microsecondsSinceEpoch)));

OUTPUT:-  11:59 AM

————————————————————————————————————————————————————————————

