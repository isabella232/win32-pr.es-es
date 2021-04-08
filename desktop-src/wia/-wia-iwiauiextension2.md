---
description: La interfaz IWiaUIExtension2 proporciona métodos que reemplazan la interfaz de usuario predeterminada proporcionada por el sistema por una interfaz de usuario personalizada y que proporcionan un icono de dispositivo personalizado.
ms.assetid: 1a747ea3-2476-438b-baf0-903b86cbbb16
title: Interfaz IWiaUIExtension2 (Wiadevd. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaUIExtension2
api_type:
- COM
api_location:
- Wiadevd.h
ms.openlocfilehash: 4bfac82f90938a89b0d0ed76d9649e8e1a7cf19c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104001183"
---
# <a name="iwiauiextension2-interface"></a>Interfaz IWiaUIExtension2

La interfaz IWiaUIExtension2 proporciona métodos que reemplazan la interfaz de usuario predeterminada proporcionada por el sistema por una interfaz de usuario personalizada y que proporcionan un icono de dispositivo personalizado. Los proveedores de dispositivos pueden implementar esta interfaz para proporcionar interfaces de usuario personalizadas para sus dispositivos.

## <a name="members"></a>Miembros

La interfaz **IWiaUIExtension2** hereda de la interfaz [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) . **IWiaUIExtension2** también tiene estos tipos de miembros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

La interfaz **IWiaUIExtension2** tiene estos métodos.



| Método                                                       | Descripción                                                                                  |
|:-------------------------------------------------------------|:---------------------------------------------------------------------------------------------|
| [**DeviceDialog**](-wia-iwiauiextension2-devicedialog.md)   | Proporciona una interfaz de usuario personalizada que reemplaza la interfaz de usuario predeterminada del sistema.<br/> |
| [**GetDeviceIcon**](-wia-iwiauiextension2-getdeviceicon.md) | Obtiene un icono de dispositivo personalizado.<br/>                                                        |



 

## <a name="remarks"></a>Observaciones



| Métodos IUnknown                                        | Descripción                               |
|---------------------------------------------------------|-------------------------------------------|
| [IUnknown:: QueryInterface](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) | Devuelve punteros a las interfaces compatibles. |
| [IUnknown:: AddRef](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref)                 | Incrementa el recuento de referencias.               |
| [IUnknown:: Release](/windows/win32/api/unknwn/nf-unknwn-iunknown-release)               | Reduce el recuento de referencias.               |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                       |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/>                                 |
| Encabezado<br/>                   | <dl> <dt>Wiadevd. h</dt> </dl> |



 

 
