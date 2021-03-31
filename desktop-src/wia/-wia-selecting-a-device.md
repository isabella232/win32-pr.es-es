---
description: Cuando una aplicación se conecta a un dispositivo de hardware de adquisición de imágenes de Windows (WIA), WIA crea un árbol de elementos (un árbol jerárquico de interfaces de IWiaItem o IWiaItem2) que representa el dispositivo y sus imágenes, carpetas y análisis de camas.
ms.assetid: 2a7bcfd4-4075-48a4-9eff-5210b9a635e3
title: Seleccionar un dispositivo (WIA)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 08a2eab41016397f6505e60efcbf78d1fdf82499
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103908001"
---
# <a name="selecting-a-device-wia"></a>Seleccionar un dispositivo (WIA)

Cuando una aplicación se conecta a un dispositivo de hardware de adquisición de imágenes de Windows (WIA), WIA crea un árbol de elementos (un árbol jerárquico de interfaces de [**IWiaItem**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem) o [**IWiaItem2**](-wia-iwiaitem2.md) ) que representa el dispositivo y sus imágenes, carpetas y análisis de camas. Una aplicación puede seleccionar y conectarse a un dispositivo sin intervención del usuario, o puede mostrar un cuadro de diálogo que permite al usuario seleccionar un dispositivo.

-   [Selección de un dispositivo sin la interfaz de usuario](#selecting-a-device-without-the-ui)
-   [Selección de un dispositivo con la interfaz de usuario](#selecting-a-device-with-the-ui)

## <a name="selecting-a-device-without-the-ui"></a>Selección de un dispositivo sin la interfaz de usuario

Realice los pasos siguientes para seleccionar y conectarse a un dispositivo de hardware WIA.

-   Llame a [CoCreateInstance](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) para recuperar un puntero a la interfaz [**IWiaDevMgr**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiadevmgr) o [**IWiaDevMgr2**](-wia-iwiadevmgr2.md) .
-   Use el método [**IWiaDevMgr:: EnumDeviceInfo**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiadevmgr-enumdeviceinfo) de la interfaz [**IWiaDevMgr**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiadevmgr) o [**IWiaDevMgr2**](-wia-iwiadevmgr2.md) para obtener un puntero a la interfaz de [**IEnumWIA \_ dev \_ info**](/windows/desktop/api/wia_xp/nn-wia_xp-ienumwia_dev_info) . Para obtener instrucciones sobre cómo enumerar dispositivos, consulte [enumerar dispositivos del sistema](-wia-enumerating-system-devices.md).
-   Use la interfaz de [**\_ \_ información de desarrollo de IEnumWIA**](/windows/desktop/api/wia_xp/nn-wia_xp-ienumwia_dev_info) para obtener punteros de interfaz de [**IWiaPropertyStorage**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiapropertystorage) para cada dispositivo WIA enumerado.
-   Use la interfaz [**IWiaPropertyStorage**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiapropertystorage) para inspeccionar las propiedades de información de dispositivos de cada dispositivo y guardar la \_ \_ \_ propiedad de ID. de dev DIP de WIA del dispositivo deseado.
-   Use la propiedad DeviceID con el método [**IWiaDevMgr:: CreateDevice**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiadevmgr-createdevice) en la interfaz [**IWiaDevMgr**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiadevmgr) o [**IWiaDevMgr2**](-wia-iwiadevmgr2.md) para crear un objeto de dispositivo WIA. El método **IWiaDevMgr:: CreateDevice** proporciona a la aplicación el puntero a la interfaz [**IWiaItem**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem) o [**IWiaItem2**](-wia-iwiaitem2.md) del elemento raíz del dispositivo especificado.

Para ver un ejemplo de cómo hacerlo en una aplicación, consulte la sección [creación de un dispositivo](-wia-creating-a-device.md) en el tutorial de esta guía.

## <a name="selecting-a-device-with-the-ui"></a>Selección de un dispositivo con la interfaz de usuario

Después de recuperar un puntero a [**IWiaDevMgr**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiadevmgr), una aplicación puede permitir que un usuario seleccione un dispositivo omitiendo el resto de los pasos anteriores y llamando a [**IWiaDevMgr:: SelectDeviceDlg**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiadevmgr-selectdevicedlg). **IWiaDevMgr:: SelectDeviceDlg** muestra un cuadro de diálogo en el que el usuario puede seleccionar un dispositivo WIA.

Se recomienda que las aplicaciones hagan que la selección de dispositivos y imágenes esté disponible a través de un elemento de menú denominado **desde el escáner** en el menú **archivo** .

 

 
