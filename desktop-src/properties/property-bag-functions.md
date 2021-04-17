---
description: En esta sección se describe un conjunto de funciones auxiliares de Windows que se usan con objetos IPropertyBag.
ms.assetid: 4ef85855-7eb6-43ec-bf29-1223eaf1a0cc
title: Funciones de contenedor de propiedades
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5c86a2e3ce61805702641f893d51f5c4aa26b0ca
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105716249"
---
# <a name="property-bag-functions"></a>Funciones de contenedor de propiedades

En esta sección se describe un conjunto de funciones auxiliares de Windows que se usan con objetos [**IPropertyBag**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768196(v=vs.85)) .



| Tema                                                                       | Contenido                                                                                                                     |
|-----------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------|
| [**PSPropertyBag \_ eliminar**](/windows/win32/api/propsys/nf-propsys-pspropertybag_delete)                     | Elimina una propiedad de un contenedor de propiedades.<br/>                                                                           |
| [**PSPropertyBag \_ ReadBOOL**](/windows/win32/api/propsys/nf-propsys-pspropertybag_readbool)                 | Lee el valor de datos **bool** de una propiedad de un contenedor de propiedades.<br/>                                                    |
| [**PSPropertyBag \_ readbstr (**](/windows/win32/api/propsys/nf-propsys-pspropertybag_readbstr)                 | Lee un valor de datos **BSTR** de una propiedad de un contenedor de propiedades.<br/>                                                    |
| [**PSPropertyBag \_ ReadDWORD**](/windows/win32/api/propsys/nf-propsys-pspropertybag_readdword)               | Lee un valor de datos **DWORD** de la propiedad en un contenedor de propiedades.<br/>                                                     |
| [**PSPropertyBag \_ ReadGUID**](/windows/win32/api/propsys/nf-propsys-pspropertybag_readguid)                 | Lee el valor de datos de GUID de una propiedad de un contenedor de propiedades.<br/>                                                      |
| [**PSPropertyBag \_ ReadInt**](/windows/win32/api/propsys/nf-propsys-pspropertybag_readint)                   | Lee un valor de datos **int** de una propiedad de un contenedor de propiedades.<br/>                                                    |
| [**PSPropertyBag \_ ReadLONG**](/windows/win32/api/propsys/nf-propsys-pspropertybag_readlong)                 | Lee un valor de datos **Long** de una propiedad de un contenedor de propiedades.<br/>                                                    |
| [**PSPropertyBag \_ ReadPOINTL**](/windows/win32/api/propsys/nf-propsys-pspropertybag_readpointl)             | Recupera las coordenadas de propiedad almacenadas en una estructura [**Pointl**](/previous-versions//dd162807(v=vs.85)) de un contenedor de propiedades especificado.<br/>    |
| [**PSPropertyBag \_ ReadPOINTS**](/windows/win32/api/propsys/nf-propsys-pspropertybag_readpoints)             | Recupera las coordenadas de propiedad almacenadas en una estructura de [**puntos**](/previous-versions//dd162808(v=vs.85)) de un contenedor de propiedades especificado.<br/>    |
| [**PSPropertyBag \_ ReadPropertyKey**](/windows/win32/api/propsys/nf-propsys-pspropertybag_readpropertykey)   | Lee la clave de propiedad de una propiedad de un contenedor de propiedades especificado.<br/>                                                 |
| [**PSPropertyBag \_ ReadRECTL**](/windows/win32/api/propsys/nf-propsys-pspropertybag_readrectl)               | Recupera las coordenadas de un rectángulo almacenado en una propiedad contenida en un contenedor de propiedades especificado.<br/>              |
| [**PSPropertyBag \_ ReadSHORT**](/windows/win32/api/propsys/nf-propsys-pspropertybag_readshort)               | Lee el valor de datos **corto** de una propiedad en un contenedor de propiedades.<br/>                                                   |
| [**PSPropertyBag \_ ReadStr**](/windows/win32/api/propsys/nf-propsys-pspropertybag_readstr)                   | Lee el valor de datos de **cadena** de una propiedad de un contenedor de propiedades.<br/>                                                  |
| [**PSPropertyBag \_ ReadStrAlloc**](/windows/win32/api/propsys/nf-propsys-pspropertybag_readstralloc)         | Lee un valor de datos de **cadena** de una propiedad de un contenedor de propiedades y asigna memoria para la cadena que se lee.<br/> |
| [**PSPropertyBag \_ ReadStream**](/windows/win32/api/propsys/nf-propsys-pspropertybag_readstream)             | Lee la secuencia de datos almacenada en una propiedad determinada contenida en un contenedor de propiedades especificado.<br/>                           |
| [**PSPropertyBag \_ ReadType**](/windows/win32/api/propsys/nf-propsys-pspropertybag_readtype)                 | Lee el tipo de valor de datos de una propiedad que está almacenada en un contenedor de propiedades.<br/>                                      |
| [**PSPropertyBag \_ ReadULONGLONG**](/windows/win32/api/propsys/nf-propsys-pspropertybag_readulonglong)       | Lee un valor de datos **ULONGLONG** de una propiedad en un contenedor de propiedades.<br/>                                               |
| [**PSPropertyBag \_ ReadUnknown**](/windows/win32/api/propsys/nf-propsys-pspropertybag_readunknown)           | Lee una propiedad determinada de un valor de datos desconocido en un contenedor de propiedades.<br/>                                                |
| [**PSPropertyBag \_ WriteBOOL**](/windows/win32/api/propsys/nf-propsys-pspropertybag_writebool)               | Establece el valor de datos **bool** de una propiedad en un contenedor de propiedades.<br/>                                                     |
| [**PSPropertyBag \_ WriteBSTR**](/windows/win32/api/propsys/nf-propsys-pspropertybag_writebstr)               | Establece un valor de datos **BSTR** a partir de una propiedad de un contenedor de propiedades.<br/>                                                     |
| [**PSPropertyBag \_ WriteDWORD**](/windows/win32/api/propsys/nf-propsys-pspropertybag_writedword)             | Establece un valor de datos **DWORD** de la propiedad en un contenedor de propiedades.<br/>                                                      |
| [**PSPropertyBag \_ WriteGUID**](/windows/win32/api/propsys/nf-propsys-pspropertybag_writeguid)               | Establece el valor de datos de GUID a partir de una propiedad de un contenedor de propiedades.<br/>                                                       |
| [**PSPropertyBag \_ WriteInt**](/windows/win32/api/propsys/nf-propsys-pspropertybag_writeint)                 | Establece un valor de datos **int** a partir de una propiedad de un contenedor de propiedades.<br/>                                                     |
| [**PSPropertyBag \_ WriteLONG**](/windows/win32/api/propsys/nf-propsys-pspropertybag_writelong)               | Establece un valor de datos **Long** a partir de una propiedad de un contenedor de propiedades.<br/>                                                     |
| [**PSPropertyBag \_ WritePOINTL**](/windows/win32/api/propsys/nf-propsys-pspropertybag_writepointl)           | Almacena las coordenadas de propiedad almacenadas en una estructura [**Pointl**](/previous-versions//dd162807(v=vs.85)) de un contenedor de propiedades especificado.<br/>       |
| [**PSPropertyBag \_ WritePOINTS**](/windows/win32/api/propsys/nf-propsys-pspropertybag_writepoints)           | Almacena las coordenadas de propiedad almacenadas en una estructura de [**puntos**](/previous-versions//dd162808(v=vs.85)) de un contenedor de propiedades especificado.<br/>       |
| [**PSPropertyBag \_ WritePropertyKey**](/windows/win32/api/propsys/nf-propsys-pspropertybag_writepropertykey) | Establece la clave de propiedad de una propiedad en un contenedor de propiedades especificado.<br/>                                                  |
| [**PSPropertyBag \_ WriteRECTL**](/windows/win32/api/propsys/nf-propsys-pspropertybag_writerectl)             | Almacena las coordenadas de un rectángulo almacenado en una propiedad contenida en un contenedor de propiedades especificado.<br/>                 |
| [**PSPropertyBag \_ WriteSHORT**](/windows/win32/api/propsys/nf-propsys-pspropertybag_writeshort)             | Establece el valor de datos **corto** de una propiedad en un contenedor de propiedades.<br/>                                                    |
| [**PSPropertyBag \_ WriteStr**](/windows/win32/api/propsys/nf-propsys-pspropertybag_writestr)                 | Establece el valor de datos de **cadena** de una propiedad de un contenedor de propiedades.<br/>                                                   |
| [**PSPropertyBag \_ WriteStream**](/windows/win32/api/propsys/nf-propsys-pspropertybag_writestream)           | Establece la secuencia de datos almacenada en una propiedad determinada contenida en un contenedor de propiedades especificado.<br/>                            |
| [**PSPropertyBag \_ WriteULONGLONG**](/windows/win32/api/propsys/nf-propsys-pspropertybag_writeulonglong)     | Establece un valor de datos **ULONGLONG** a partir de una propiedad de un contenedor de propiedades.<br/>                                                |
| [**PSPropertyBag \_ WriteUnknown**](/windows/win32/api/propsys/nf-propsys-pspropertybag_writeunknown)         | Establece una propiedad determinada de un valor de datos desconocido en un contenedor de propiedades.<br/>                                                 |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Funciones PROPVARIANT y VARIANT](./functions-propvarutil.md)
</dt> <dt>

[Funciones](functions.md)
</dt> </dl>

 

 
