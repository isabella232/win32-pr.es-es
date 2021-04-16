---
description: Todas las propiedades de una clase de vista deben tener un calificador de matriz de cadenas denominado PropertySources.
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
ms.openlocfilehash: 3809977282a2bdf82d0b51ef8f566541b74fe28a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105715465"
---
# <a name="propertysources-qualifier"></a>Calificador PropertySources

Todas las propiedades de una clase de vista deben tener un calificador de matriz de cadenas denominado **PropertySources**. El calificador **PropertySources** contiene el nombre de la propiedad o propiedades de clase de origen de la que obtiene datos esta propiedad de clase de vista. El orden de los valores de esta matriz se corresponde con el orden de las clases de origen definidas para el [calificador ViewSources](viewsources-qualifier.md). En el ejemplo siguiente se muestra cómo definir una propiedad para una clase de vista de Unión que es la Unión de la clase [**Win32 \_ LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) de dos equipos diferentes:


```mof
[PropertySources{"DeviceID", "DeviceID"},key] String Devname;
```



La primera propiedad **DeviceID** corresponde a la propiedad **DeviceID** de la clase en la primera consulta de origen. La segunda propiedad **DeviceID** es la propiedad **DeviceID** de la clase en la segunda consulta de origen.

Al definir las propiedades de las clases de vista de combinación, debe definir una propiedad de vista independiente para cada una de las propiedades de la clase de origen a menos que las propiedades de la clase de origen sean la base de la clase de vista de combinación. En el ejemplo siguiente se crean propiedades en una clase de vista de combinación en propiedades similares de la clase de origen de [**\_ impresora Win32**](/windows/desktop/CIMWin32Prov/win32-printer) y la clase de origen [**\_ PrinterConfiguration de Win32**](/windows/desktop/CIMWin32Prov/win32-printerconfiguration) :


```mof
[PropertySources{"VerticalResolution", ""}] Uint32 Vres;
[PropertySources{"", "YResolution"}] Uint32 Yres;
```



Si las dos clases de origen se combinan mediante una propiedad común, solo se puede definir una propiedad de clase de vista, ya que el valor de ambas propiedades de clase de origen siempre es el mismo. En el ejemplo siguiente se muestra cómo unir la clase de [**\_ impresora Win32**](/windows/desktop/CIMWin32Prov/win32-printer) y la [**\_ PrinterConfiguration Win32**](/windows/desktop/CIMWin32Prov/win32-printerconfiguration) mediante un valor de propiedad común:


```mof
[PropertySources{"DeviceId", "DeviceName "}] String Name;
```



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|--------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>       |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Calificadores específicos del proveedor de vistas**](qualifiers-specific-to-the-view-provider.md)
</dt> </dl>

 

