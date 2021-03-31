---
title: Las interfaces IADs y IDirectoryObject
description: Los clientes ADSI administran y manipulan los objetos de servicio de directorio mediante el uso de una de las dos interfaces COM IADs o IDirectoryObject.
ms.assetid: f9c486b0-3dfb-4abf-afbf-08749e04315f
ms.tgt_platform: multiple
keywords:
- ADSI de IADs, acerca de
- IDirectoryObject ADSI, acerca de
- ADSI ADSI, usar interfaces IADs y IDirectoryObject
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 32dfef47fe1c66e4303725deecec14fe93d1fd92
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/21/2020
ms.locfileid: "103904826"
---
# <a name="the-iads-and-idirectoryobject-interfaces"></a>Las interfaces IADs y IDirectoryObject

Los clientes ADSI administran y manipulan objetos del servicio de directorio mediante una de las dos interfaces COM: [**IADs**](/windows/desktop/api/Iads/nn-iads-iads) o [**IDirectoryObject**](/windows/desktop/api/Iads/nn-iads-idirectoryobject). **IADs** es una interfaz [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) diseñada para su uso por parte de clientes enlazados en tiempo de ejecución, como los escritos en Microsoft Visual Basic, Java y varios lenguajes de scripting. **IDirectoryObject** es una interfaz vtable que proporciona acceso directo a los objetos por parte de los clientes enlazados en tiempo de compilación, como los escritos en C y C++.

Cada objeto ADSI debe implementar [**IADs**](/windows/desktop/api/Iads/nn-iads-iads) y [**IDirectoryObject**](/windows/desktop/api/Iads/nn-iads-idirectoryobject). Los clientes ADSI escritos en lenguajes como C o C++, que pueden tener acceso directamente a vtables, pueden utilizar cualquiera de las interfaces, pero no ambas en la misma aplicación. Los clientes ADSI escritos en Visual Basic o Java se limitan al uso de **IADs**.

La interfaz [**IADs**](/windows/desktop/api/Iads/nn-iads-iads) permite que los clientes enlazados en tiempo de ejecución aprovechen las características de mantenimiento inherentes del modelo de objetos ADSI. Entre estas características se encuentra la memoria caché de propiedades, que permite a los clientes leer y escribir propiedades sin pasar por la conexión para cada llamada. Además, las aplicaciones cliente obtienen el uso de eficaces bibliotecas de interfaz de usuario y controles ActiveX y un estilo más sencillo de programación. En la devolución, los clientes enlazados en tiempo de ejecución deben usar el tipo de datos **Variant** , lo que impide el uso de los tipos de datos nativos más completos proporcionados por ADSI.

La interfaz [**IDirectoryObject**](/windows/desktop/api/Iads/nn-iads-idirectoryobject) permite a los clientes enlazados en tiempo de compilación sacar el máximo partido de los tipos de datos nativos de servicios de directorio a costa de una ligera ventaja de rendimiento de usar la memoria caché de propiedades. A cambio, la interfaz **IDirectoryObject** proporciona acceso directo y en el cable a las propiedades de objeto a través de una única solicitud, en lugar de a través de llamadas **Get** y **Put** individuales.

 

 