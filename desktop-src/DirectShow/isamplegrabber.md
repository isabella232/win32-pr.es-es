---
description: El filtro Sample Grabber expone la interfaz ISampleGrabber. Permite a una aplicación recuperar muestras de medios individuales a medida que se mueven por el gráfico de filtro.
ms.assetid: 97cf1127-d5d7-4e6a-a371-19f24e497a7f
title: Interfaz ISampleGrabber (Qedit.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISampleGrabber
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: f6e923032e74f88dceb1c2465e27dab9423bae1c
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127255110"
---
# <a name="isamplegrabber-interface"></a>ISampleGrabber (interfaz)

> [!Note]  
> \[En desuso. Esta API puede quitarse de futuras versiones de Windows.\]

 

El filtro Sample [**Grabber**](sample-grabber-filter.md) expone la interfaz **ISampleGrabber.** Permite a una aplicación recuperar muestras de medios individuales a medida que se mueven por el gráfico de filtro.

## <a name="members"></a>Members

La **interfaz ISampleGrabber** hereda de la [**interfaz IUnknown.**](/windows/win32/api/unknwn/nn-unknwn-iunknown) **ISampleGrabber** también tiene estos tipos de miembros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

La **interfaz ISampleGrabber** tiene estos métodos.



| Método                                                                | Descripción                                                                                                                       |
|:----------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------|
| [**GetConnectedMediaType**](isamplegrabber-getconnectedmediatype.md) | Recupera el tipo de medio para la conexión en el pin de entrada de Sample Grabber.<br/>                                        |
| [**GetCurrentBuffer**](isamplegrabber-getcurrentbuffer.md)           | Recupera una copia del ejemplo que el filtro recibió más recientemente.<br/>                                                 |
| [**GetCurrentSample**](isamplegrabber-getcurrentsample.md)           | Sin implementar.<br/>                                                                                                       |
| [**SetBufferSamples**](isamplegrabber-setbuffersamples.md)           | Especifica si se copian datos de ejemplo en un búfer a medida que pasan por el filtro.<br/>                                     |
| [**SetCallback**](isamplegrabber-setcallback.md)                     | Especifica un método de devolución de llamada para llamar a en los ejemplos entrantes.<br/>                                                               |
| [**SetMediaType**](isamplegrabber-setmediatype.md)                   | Especifica el tipo de medio para la conexión en el pin de entrada de Sample Grabber.<br/>                                    |
| [**SetOneShot**](isamplegrabber-setoneshot.md)                       | Especifica si el filtro [**Sample Grabber**](sample-grabber-filter.md) se detiene después de que el filtro reciba una muestra.<br/> |



 

## <a name="remarks"></a>Observaciones

> [!Note]  
> El archivo de encabezado Qedit.h no es compatible con los encabezados de Direct3D posteriores a la versión 7.

 

> [!Note]  
> Para obtener Qedit.h, descargue la actualización del SDK de Microsoft Windows para [Windows Vista y .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx). Qedit.h no está disponible en el SDK de Microsoft Windows para Windows 7 y .NET Framework 3.5 Service Pack 1.

 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|-----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Qedit.h</dt> </dl>      |
| Biblioteca<br/> | <dl> <dt>Strmiids.lib</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Uso de Sample Grabber](using-the-sample-grabber.md)
</dt> </dl>

 

 
