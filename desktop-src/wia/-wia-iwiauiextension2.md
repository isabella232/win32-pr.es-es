---
description: La interfaz IWiaUIExtension2 proporciona métodos que reemplazan la interfaz de usuario predeterminada proporcionada por el sistema por una interfaz de usuario personalizada y que proporcionan un icono de dispositivo personalizado.
ms.assetid: 1a747ea3-2476-438b-baf0-903b86cbbb16
title: Interfaz IWiaUIExtension2 (Wiadevd.h)
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
ms.openlocfilehash: 2111c25a83a9b826f4cab7dba8f689e01a9868ac416b8fb3026f1b1fb49a90ec
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118208148"
---
# <a name="iwiauiextension2-interface"></a>Interfaz IWiaUIExtension2

La interfaz IWiaUIExtension2 proporciona métodos que reemplazan la interfaz de usuario predeterminada proporcionada por el sistema por una interfaz de usuario personalizada y que proporcionan un icono de dispositivo personalizado. Los proveedores de dispositivos pueden implementar esta interfaz para proporcionar interfaces de usuario personalizadas para sus dispositivos.

## <a name="members"></a>Miembros

La **interfaz IWiaUIExtension2** hereda de la [**interfaz IUnknown.**](/windows/win32/api/unknwn/nn-unknwn-iunknown) **IWiaUIExtension2** también tiene estos tipos de miembros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

La **interfaz IWiaUIExtension2** tiene estos métodos.



| Método                                                       | Descripción                                                                                  |
|:-------------------------------------------------------------|:---------------------------------------------------------------------------------------------|
| [**DeviceDialog**](-wia-iwiauiextension2-devicedialog.md)   | Proporciona una interfaz de usuario personalizada que reemplaza a la interfaz de usuario predeterminada del sistema.<br/> |
| [**GetDeviceIcon**](-wia-iwiauiextension2-getdeviceicon.md) | Obtiene un icono de dispositivo personalizado.<br/>                                                        |



 

## <a name="remarks"></a>Comentarios



| Métodos IUnknown                                        | Descripción                               |
|---------------------------------------------------------|-------------------------------------------|
| [IUnknown::QueryInterface](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) | Devuelve punteros a las interfaces compatibles. |
| [IUnknown::AddRef](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref)                 | Incrementa el recuento de referencias.               |
| [IUnknown::Release](/windows/win32/api/unknwn/nf-unknwn-iunknown-release)               | Reduce el recuento de referencias.               |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                       |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                 |
| Header<br/>                   | <dl> <dt>Wiadevd.h</dt> </dl> |



 

 
