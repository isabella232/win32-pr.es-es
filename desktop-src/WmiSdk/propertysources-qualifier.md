---
description: Cada propiedad de una clase de vista debe tener un calificador de matriz de cadenas denominado PropertySources.
ms.assetid: df89680b-8ea7-4f38-81ba-c4132b944f37
ms.tgt_platform: multiple
title: Calificador PropertySources
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PropertySources
api_type:
- NA
api_location: ''
ms.openlocfilehash: 95f7fbb06a8d61f2a046a720a28d348a43b6a639ceef34e04b2e1fd813a96766
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118817624"
---
# <a name="propertysources-qualifier"></a>Calificador PropertySources

Cada propiedad de una clase de vista debe tener un calificador de matriz de cadenas denominado **PropertySources.** El **calificador PropertySources** contiene el nombre de la propiedad o propiedades de clase de origen de las que esta propiedad de clase de vista obtiene datos. El orden de los valores de esta matriz corresponde al orden de las clases de origen definidas para el [calificador ViewSources](viewsources-qualifier.md). En el ejemplo siguiente se muestra cómo definir una propiedad para una clase de vista de unión que es la unión de la clase [**\_ LogicalDisk win32**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) desde dos equipos diferentes:


```mof
[PropertySources{"DeviceID", "DeviceID"},key] String Devname;
```



La primera **propiedad DeviceID** corresponde a la **propiedad DeviceID** de la clase de la primera consulta de origen. La segunda **propiedad DeviceID** es la **propiedad DeviceID** de la clase en la segunda consulta de origen.

Al definir propiedades para las clases de vista de combinación, debe definir una propiedad de vista independiente para cada una de las propiedades de clase de origen a menos que las propiedades de clase de origen sean la base de la clase de vista de combinación. En el ejemplo siguiente se crean propiedades en una clase de vista de combinación en propiedades similares de la clase de origen Printer de [**Win32 \_**](/windows/desktop/CIMWin32Prov/win32-printer) y la clase de origen [**\_ PrinterConfiguration de Win32:**](/windows/desktop/CIMWin32Prov/win32-printerconfiguration)


```mof
[PropertySources{"VerticalResolution", ""}] Uint32 Vres;
[PropertySources{"", "YResolution"}] Uint32 Yres;
```



Si las dos clases de origen están unidas por una propiedad común, solo puede definir una propiedad de clase de vista única porque el valor de ambas propiedades de clase de origen siempre es el mismo. En el ejemplo siguiente se muestra cómo unir la clase Printer de [**Win32 \_**](/windows/desktop/CIMWin32Prov/win32-printer) y [**Win32 \_ PrinterConfiguration**](/windows/desktop/CIMWin32Prov/win32-printerconfiguration) mediante un valor de propiedad común:


```mof
[PropertySources{"DeviceId", "DeviceName "}] String Name;
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>       |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Calificadores específicos del proveedor de vistas**](qualifiers-specific-to-the-view-provider.md)
</dt> </dl>

 

