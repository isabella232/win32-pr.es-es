---
title: Interfaces IAD e IDirectoryObject
description: Los clientes ADSI administran y manipulan objetos de servicio de directorio mediante uno de los dos IAD de interfaces COM o IDirectoryObject.
ms.assetid: f9c486b0-3dfb-4abf-afbf-08749e04315f
ms.tgt_platform: multiple
keywords:
- ADSI de IADs , acerca de
- IDirectoryObject ADSI , acerca de
- ADSI ADSI , using, IADs e interfaces IDirectoryObject
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 32dfef47fe1c66e4303725deecec14fe93d1fd92
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127062759"
---
# <a name="the-iads-and-idirectoryobject-interfaces"></a>Interfaces IAD e IDirectoryObject

Los clientes ADSI administran y manipulan objetos de servicio de directorio mediante una de las dos interfaces COM: [**IAD o**](/windows/desktop/api/Iads/nn-iads-iads) [**IDirectoryObject**](/windows/desktop/api/Iads/nn-iads-idirectoryobject). **Los IAD son** una interfaz [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) diseñada para su uso por clientes enlazados en tiempo de ejecución, como los escritos en Microsoft Visual Basic, Java y varios lenguajes de scripting. **IDirectoryObject** es una interfaz de vtable que proporciona acceso directo a objetos por parte de clientes enlazados tempranamente, como los escritos en C y C++.

Cada objeto ADSI debe implementar [**los IAD e**](/windows/desktop/api/Iads/nn-iads-iads) [**IDirectoryObject**](/windows/desktop/api/Iads/nn-iads-idirectoryobject). Los clientes ADSI escritos en lenguajes como C o C++, que pueden acceder directamente a las vtables, pueden usar cualquiera de las interfaces, pero no ambas en la misma aplicación. Los clientes ADSI escritos Visual Basic o Java se limitan al uso de **los IAD.**

La [**interfaz IAD permite**](/windows/desktop/api/Iads/nn-iads-iads) a los clientes enlazados en tiempo de tarde aprovechar las características inherentes de mantenimiento del modelo de objetos ADSI. Entre estas características se encuentra la caché de propiedades, que permite a los clientes leer y escribir propiedades sin pasar por la conexión para cada llamada. Además, las aplicaciones cliente obtienen el uso de eficaces bibliotecas de interfaz de usuario ActiveX control y un estilo de programación más sencillo. A cambio, los clientes enlazados en tiempo de tarde deben usar el tipo de datos **VARIANT,** lo que impide el uso de los tipos de datos nativos más completos proporcionados por ADSI.

La [**interfaz IDirectoryObject**](/windows/desktop/api/Iads/nn-iads-idirectoryobject) permite a los clientes enlazados en tiempo de ejecución aprovechar al máximo los tipos de datos nativos del servicio de directorio a costa de perder una ligera ventaja de rendimiento al usar la caché de propiedades. A cambio, la **interfaz IDirectoryObject** proporciona acceso directo y en línea a las propiedades del objeto a través de una única solicitud, en lugar de a través de llamadas **get** y **put** individuales.

 

 