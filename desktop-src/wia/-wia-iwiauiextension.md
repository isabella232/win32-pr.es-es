---
description: La interfaz IWiaUIExtension proporciona métodos que reemplazan la interfaz de usuario predeterminada del sistema, proporcionan un logotipo de mapa de bits de dispositivo personalizado y proporcionan un icono de dispositivo personalizado.
ms.assetid: e3c69019-0e07-44ad-b48b-ea7e3daed2b7
title: Interfaz IWiaUIExtension (Wiadevd. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaUIExtension
api_type:
- COM
api_location:
- Wiadevd.h
ms.openlocfilehash: 98318ba3b2b94d334834150b219c5d453c4e0d89
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105720366"
---
# <a name="iwiauiextension-interface"></a>Interfaz IWiaUIExtension

La interfaz **IWiaUIExtension** proporciona métodos que reemplazan la interfaz de usuario predeterminada del sistema, proporcionan un logotipo de mapa de bits de dispositivo personalizado y proporcionan un icono de dispositivo personalizado.

## <a name="members"></a>Miembros

La interfaz **IWiaUIExtension** hereda de la interfaz [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) . **IWiaUIExtension** también tiene estos tipos de miembros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

La interfaz **IWiaUIExtension** tiene estos métodos.



| Método                                                                  | Descripción                                                                                  |
|:------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------|
| [**DeviceDialog**](-wia-iwiauiextension-devicedialog.md)               | Proporciona una interfaz de usuario personalizada que reemplaza la interfaz de usuario predeterminada del sistema.<br/> |
| [**GetDeviceBitmapLogo**](-wia-iwiauiextension-getdevicebitmaplogo.md) | Obtiene un logotipo de mapa de bits personalizado para el dispositivo.<br/>                                         |
| [**GetDeviceIcon**](-wia-iwiauiextension-getdeviceicon.md)             | Obtiene un icono de dispositivo personalizado.<br/>                                                        |



 

## <a name="remarks"></a>Observaciones



| Métodos IUnknown                                        | Descripción                               |
|---------------------------------------------------------|-------------------------------------------|
| [IUnknown:: QueryInterface](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) | Devuelve punteros a las interfaces compatibles. |
| [IUnknown:: AddRef](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref)                 | Incrementa el recuento de referencias.               |
| [IUnknown:: Release](/windows/win32/api/unknwn/nf-unknwn-iunknown-release)               | Reduce el recuento de referencias.               |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows XP \[\]<br/>                                          |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                 |
| Encabezado<br/>                   | <dl> <dt>Wiadevd. h</dt> </dl> |



 

 
