---
description: En esta sección se describe un conjunto de funciones auxiliares de Windows usadas con objetos IPropertyBag.
ms.assetid: 4ef85855-7eb6-43ec-bf29-1223eaf1a0cc
title: Funciones del bolsa de propiedades
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b694c579c76be96b00fa8392344ac59bdc0ce42f
ms.sourcegitcommit: f848119a8faa29b27585f4df53f6e50ee9666684
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/27/2021
ms.locfileid: "110550200"
---
# <a name="property-bag-functions"></a>Funciones del bolsa de propiedades

En esta sección se describe un conjunto de funciones auxiliares de Windows usadas con [**objetos IPropertyBag.**](/windows/win32/api/oaidl/nn-oaidl-ipropertybag)



| Tema                                                                       | Contenido                                                                                                                     |
|-----------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------|
| [**PSPropertyBag \_ Delete**](/windows/win32/api/propsys/nf-propsys-pspropertybag_delete)                     | Elimina una propiedad de un bolsa de propiedades.<br/>                                                                           |
| [**PSPropertyBag \_ ReadBOOL**](/windows/win32/api/propsys/nf-propsys-pspropertybag_readbool)                 | Lee el valor **de datos BOOL** de una propiedad en un bolsa de propiedades.<br/>                                                    |
| [**PSPropertyBag \_ ReadBSTR**](/windows/win32/api/propsys/nf-propsys-pspropertybag_readbstr)                 | Lee un valor **de datos BSTR** de una propiedad en un bolsa de propiedades.<br/>                                                    |
| [**PSPropertyBag \_ ReadDWORD**](/windows/win32/api/propsys/nf-propsys-pspropertybag_readdword)               | Lee un valor **de datos DWORD** de la propiedad en un bolsa de propiedades.<br/>                                                     |
| [**PSPropertyBag \_ ReadGUID**](/windows/win32/api/propsys/nf-propsys-pspropertybag_readguid)                 | Lee el valor de datos GUID de una propiedad en un bolsa de propiedades.<br/>                                                      |
| [**PSPropertyBag \_ ReadInt**](/windows/win32/api/propsys/nf-propsys-pspropertybag_readint)                   | Lee un valor **de datos int** de una propiedad en un bolsa de propiedades.<br/>                                                    |
| [**PSPropertyBag \_ ReadLONG**](/windows/win32/api/propsys/nf-propsys-pspropertybag_readlong)                 | Lee un valor **de datos LONG** de una propiedad en un bolsa de propiedades.<br/>                                                    |
| [**PSPropertyBag \_ ReadPOINTL**](/windows/win32/api/propsys/nf-propsys-pspropertybag_readpointl)             | Recupera las coordenadas de propiedad almacenadas en una [**estructura POINTL**](/previous-versions//dd162807(v=vs.85)) de un bolsa de propiedades especificado.<br/>    |
| [**PSPropertyBag \_ ReadPOINTS**](/windows/win32/api/propsys/nf-propsys-pspropertybag_readpoints)             | Recupera las coordenadas de propiedad almacenadas en una [**estructura POINTS**](/previous-versions//dd162808(v=vs.85)) de un bolsa de propiedades especificado.<br/>    |
| [**PSPropertyBag \_ ReadPropertyKey**](/windows/win32/api/propsys/nf-propsys-pspropertybag_readpropertykey)   | Lee la clave de propiedad de una propiedad en un bolsa de propiedades especificado.<br/>                                                 |
| [**PSPropertyBag \_ ReadRECTL**](/windows/win32/api/propsys/nf-propsys-pspropertybag_readrectl)               | Recupera las coordenadas de un rectángulo almacenado en una propiedad contenida en un bolsa de propiedades especificado.<br/>              |
| [**PSPropertyBag \_ ReadSHORT**](/windows/win32/api/propsys/nf-propsys-pspropertybag_readshort)               | Lee el valor **de datos SHORT** de una propiedad en un bolsa de propiedades.<br/>                                                   |
| [**PSPropertyBag \_ ReadStr**](/windows/win32/api/propsys/nf-propsys-pspropertybag_readstr)                   | Lee el valor **de datos** de cadena de una propiedad en un bolsa de propiedades.<br/>                                                  |
| [**PSPropertyBag \_ ReadStrAlloc**](/windows/win32/api/propsys/nf-propsys-pspropertybag_readstralloc)         | Lee un valor **de datos** de cadena de una propiedad en un bolsa de propiedades y asigna memoria para la cadena que se lee.<br/> |
| [**PSPropertyBag \_ ReadStream**](/windows/win32/api/propsys/nf-propsys-pspropertybag_readstream)             | Lee el flujo de datos almacenado en una propiedad determinada contenida en un bolsa de propiedades especificado.<br/>                           |
| [**PSPropertyBag \_ ReadType**](/windows/win32/api/propsys/nf-propsys-pspropertybag_readtype)                 | Lee el tipo de valor de datos de una propiedad que se almacena en un bolsa de propiedades.<br/>                                      |
| [**PSPropertyBag \_ ReadULONGLONG**](/windows/win32/api/propsys/nf-propsys-pspropertybag_readulonglong)       | Lee un valor **de datos ULONGLONG** de una propiedad en un bolsa de propiedades.<br/>                                               |
| [**PSPropertyBag \_ ReadUnknown**](/windows/win32/api/propsys/nf-propsys-pspropertybag_readunknown)           | Lee una propiedad determinada de un valor de datos desconocido en un bolsa de propiedades.<br/>                                                |
| [**PSPropertyBag \_ WriteBOOL**](/windows/win32/api/propsys/nf-propsys-pspropertybag_writebool)               | Establece el **valor de datos BOOL** de una propiedad en un bolsa de propiedades.<br/>                                                     |
| [**PSPropertyBag \_ WriteBSTR**](/windows/win32/api/propsys/nf-propsys-pspropertybag_writebstr)               | Establece un **valor de datos BSTR** de una propiedad en un bolsa de propiedades.<br/>                                                     |
| [**PSPropertyBag \_ WriteDWORD**](/windows/win32/api/propsys/nf-propsys-pspropertybag_writedword)             | Establece un **valor de datos DWORD** de la propiedad en un bolsa de propiedades.<br/>                                                      |
| [**PSPropertyBag \_ WriteGUID**](/windows/win32/api/propsys/nf-propsys-pspropertybag_writeguid)               | Establece el valor de datos GUID de una propiedad en un bolsa de propiedades.<br/>                                                       |
| [**PSPropertyBag \_ WriteInt**](/windows/win32/api/propsys/nf-propsys-pspropertybag_writeint)                 | Establece un **valor de** datos int de una propiedad en un bolsa de propiedades.<br/>                                                     |
| [**PSPropertyBag \_ WriteLONG**](/windows/win32/api/propsys/nf-propsys-pspropertybag_writelong)               | Establece un **valor de** datos LONG de una propiedad en un bolsa de propiedades.<br/>                                                     |
| [**PSPropertyBag \_ WritePOINTL**](/windows/win32/api/propsys/nf-propsys-pspropertybag_writepointl)           | Almacena las coordenadas de propiedad almacenadas en una [**estructura POINTL**](/previous-versions//dd162807(v=vs.85)) de un bolsa de propiedades especificado.<br/>       |
| [**PSPropertyBag \_ WritePOINTS**](/windows/win32/api/propsys/nf-propsys-pspropertybag_writepoints)           | Almacena las coordenadas de propiedad almacenadas en una [**estructura POINTS**](/previous-versions//dd162808(v=vs.85)) de un bolsa de propiedades especificado.<br/>       |
| [**PSPropertyBag \_ WritePropertyKey**](/windows/win32/api/propsys/nf-propsys-pspropertybag_writepropertykey) | Establece la clave de propiedad de una propiedad en un bolsa de propiedades especificado.<br/>                                                  |
| [**PSPropertyBag \_ WriteRECTL**](/windows/win32/api/propsys/nf-propsys-pspropertybag_writerectl)             | Almacena las coordenadas de un rectángulo almacenado en una propiedad contenida en un bolsa de propiedades especificado.<br/>                 |
| [**PSPropertyBag \_ WriteSHORT**](/windows/win32/api/propsys/nf-propsys-pspropertybag_writeshort)             | Establece el **valor de** datos SHORT de una propiedad en un bolsa de propiedades.<br/>                                                    |
| [**PSPropertyBag \_ WriteStr**](/windows/win32/api/propsys/nf-propsys-pspropertybag_writestr)                 | Establece el **valor de datos** de cadena de una propiedad en un bolsa de propiedades.<br/>                                                   |
| [**PSPropertyBag \_ WriteStream**](/windows/win32/api/propsys/nf-propsys-pspropertybag_writestream)           | Establece el flujo de datos almacenado en una propiedad determinada contenida en un bolsa de propiedades especificado.<br/>                            |
| [**PSPropertyBag \_ WriteULONGLONG**](/windows/win32/api/propsys/nf-propsys-pspropertybag_writeulonglong)     | Establece un **valor de datos ULONGLONG** de una propiedad en un bolsa de propiedades.<br/>                                                |
| [**PSPropertyBag \_ WriteUnknown**](/windows/win32/api/propsys/nf-propsys-pspropertybag_writeunknown)         | Establece una propiedad determinada de un valor de datos desconocido en un bolsa de propiedades.<br/>                                                 |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Funciones PROPVARIANT y VARIANT](./functions-propvarutil.md)
</dt> <dt>

[Funciones](functions.md)
</dt> </dl>

 

 
