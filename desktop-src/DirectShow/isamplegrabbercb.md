---
description: La interfaz ISampleGrabberCB proporciona métodos de devolución de llamada para el método ISampleGrabber::SetCallback. Si la aplicación llama a ese método, debe implementar esta interfaz. Para obtener más información, vea ISampleGrabber.
ms.assetid: 30166d1b-cc37-43c4-8f64-681d8f2013b9
title: Interfaz ISampleGrabberCB (Qedit.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISampleGrabberCB
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 5c39d11e6560bc5e50a4c8a9b42a1cbb095b4b71
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127063250"
---
# <a name="isamplegrabbercb-interface"></a>Interfaz ISampleGrabberCB

> [!Note]  
> \[Obsoleto. Esta API puede quitarse de futuras versiones de Windows.\]

 

La `ISampleGrabberCB` interfaz proporciona métodos de devolución de llamada [**para el método ISampleGrabber::SetCallback.**](isamplegrabber-setcallback.md) Si la aplicación llama a ese método, debe implementar esta interfaz. Para obtener más información, [**vea ISampleGrabber**](isamplegrabber.md).

## <a name="members"></a>Members

La **interfaz ISampleGrabberCB** hereda de la [**interfaz IUnknown.**](/windows/win32/api/unknwn/nn-unknwn-iunknown) **ISampleGrabberCB** también tiene estos tipos de miembros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

La **interfaz ISampleGrabberCB** tiene estos métodos.



| Método                                        | Descripción                                                              |
|:----------------------------------------------|:-------------------------------------------------------------------------|
| [**BufferCB**](isamplegrabbercb-buffercb.md) | Método de devolución de llamada que recibe un puntero al búfer de ejemplo.<br/> |
| [**SampleCB**](isamplegrabbercb-samplecb.md) | Método de devolución de llamada que recibe un puntero al ejemplo multimedia.<br/>  |



 

## <a name="remarks"></a>Observaciones

> [!Note]  
> El archivo de encabezado Qedit.h no es compatible con los encabezados de Direct3D posteriores a la versión 7.

 

> [!Note]  
> Para obtener Qedit.h, descargue la actualización del SDK de [Microsoft Windows para Windows Vista y .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx). Qedit.h no está disponible en el SDK de Microsoft Windows para Windows 7 y .NET Framework 3.5 Service Pack 1.

 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|-----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Qedit.h</dt> </dl>      |
| Biblioteca<br/> | <dl> <dt>Strmiids.lib</dt> </dl> |



 

 
