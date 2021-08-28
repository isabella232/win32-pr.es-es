---
title: IMsTscAdvancedSettings IconIndex, propiedad
description: Especifica el índice del icono en el archivo de icono actual.
ms.assetid: c29ae1a7-9c54-4e56-bb69-4e929e8a4e5c
ms.tgt_platform: multiple
keywords:
- Propiedad IconIndex Servicios de Escritorio remoto
- Propiedad IconIndex Servicios de Escritorio remoto interfaz , IMsTscAdvancedSettings
- Interfaz IMsTscAdvancedSettings Servicios de Escritorio remoto propiedad , IconIndex
- Propiedad IconIndex Servicios de Escritorio remoto interfaz , IMsRdpClientAdvancedSettings
- Interfaz IMsRdpClientAdvancedSettings Servicios de Escritorio remoto propiedad , IconIndex
- Propiedad IconIndex Servicios de Escritorio remoto interfaz , IMsRdpClientAdvancedSettings2
- Interfaz IMsRdpClientAdvancedSettings2 Servicios de Escritorio remoto propiedad , IconIndex
- Propiedad IconIndex Servicios de Escritorio remoto interfaz , IMsRdpClientAdvancedSettings3
- Interfaz IMsRdpClientAdvancedSettings3 Servicios de Escritorio remoto propiedad , IconIndex
- Propiedad IconIndex Servicios de Escritorio remoto interfaz , IMsRdpClientAdvancedSettings4
- Interfaz IMsRdpClientAdvancedSettings4 Servicios de Escritorio remoto propiedad , IconIndex
- Propiedad IconIndex Servicios de Escritorio remoto interfaz , IMsRdpClientAdvancedSettings5
- Interfaz IMsRdpClientAdvancedSettings5 Servicios de Escritorio remoto propiedad , IconIndex
- Propiedad IconIndex Servicios de Escritorio remoto interfaz , IMsRdpClientAdvancedSettings6
- Interfaz IMsRdpClientAdvancedSettings6 Servicios de Escritorio remoto propiedad , IconIndex
- Propiedad IconIndex Servicios de Escritorio remoto interfaz , IMsRdpClientAdvancedSettings7
- Interfaz IMsRdpClientAdvancedSettings7 Servicios de Escritorio remoto propiedad , IconIndex
- Propiedad IconIndex Servicios de Escritorio remoto interfaz , IMsRdpClientAdvancedSettings8
- Interfaz IMsRdpClientAdvancedSettings8 Servicios de Escritorio remoto propiedad , IconIndex
topic_type:
- apiref
api_name:
- IMsTscAdvancedSettings.IconIndex
- IMsTscAdvancedSettings.put_IconIndex
- IMsRdpClientAdvancedSettings.IconIndex
- IMsRdpClientAdvancedSettings.put_IconIndex
- IMsRdpClientAdvancedSettings2.IconIndex
- IMsRdpClientAdvancedSettings2.put_IconIndex
- IMsRdpClientAdvancedSettings3.IconIndex
- IMsRdpClientAdvancedSettings3.put_IconIndex
- IMsRdpClientAdvancedSettings4.IconIndex
- IMsRdpClientAdvancedSettings4.put_IconIndex
- IMsRdpClientAdvancedSettings5.IconIndex
- IMsRdpClientAdvancedSettings5.put_IconIndex
- IMsRdpClientAdvancedSettings6.IconIndex
- IMsRdpClientAdvancedSettings6.put_IconIndex
- IMsRdpClientAdvancedSettings7.IconIndex
- IMsRdpClientAdvancedSettings7.put_IconIndex
- IMsRdpClientAdvancedSettings8.IconIndex
- IMsRdpClientAdvancedSettings8.put_IconIndex
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a7c1c53a073f218666ab44eb926b9a92f835078c50a88bc488cc1da4b70b056f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120125465"
---
# <a name="imstscadvancedsettingsiconindex-property"></a>IMsTscAdvancedSettings::IconIndex, propiedad

Especifica el índice del icono en el archivo de icono actual.

> [!Note]  
> Esta propiedad no se admite en el control ActiveX (MsRdp.ocx). Se admite en la biblioteca MsTscAx.dll que se incluye en el cliente estándar (MsTsc.exe).

 

Esta propiedad es de solo escritura.

## <a name="syntax"></a>Syntax


```C++
HRESULT put_IconIndex(
  [in] LONG IconIndex
);
```



## <a name="property-value"></a>Valor de propiedad

Índice del icono.

## <a name="error-codes"></a>Códigos de error

Devuelve **S \_ FALSE.**

## <a name="remarks"></a>Comentarios

Para obtener más información sobre Conexión web a Escritorio remoto, vea [Requisitos para Conexión web a Escritorio remoto](requirements-for-remote-desktop-web-connection.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                                  |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                            |
| Biblioteca de tipos<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>    |
| Archivo DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>    |
| IID<br/>                      | IID \_ IMsTscAdvancedSettings se define como 809945cc-4b3b-4a92-a6b0-dbf9b5f2ef2d<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IMsRdpClientAdvancedSettings**](imsrdpclientadvancedsettings-interface.md)
</dt> <dt>

[**IMsRdpClientAdvancedSettings2**](imsrdpclientadvancedsettings2.md)
</dt> <dt>

[**IMsRdpClientAdvancedSettings3**](imsrdpclientadvancedsettings3.md)
</dt> <dt>

[**IMsRdpClientAdvancedSettings4**](imsrdpclientadvancedsettings4.md)
</dt> <dt>

[**IMsRdpClientAdvancedSettings5**](imsrdpclientadvancedsettings5.md)
</dt> <dt>

[**IMsRdpClientAdvancedSettings6**](imsrdpclientadvancedsettings6.md)
</dt> <dt>

[**IMsRdpClientAdvancedSettings7**](imsrdpclientadvancedsettings7.md)
</dt> <dt>

[**IMsRdpClientAdvancedSettings8**](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[**IMsTscAdvancedSettings**](imstscadvancedsettings-interface.md)
</dt> </dl>

 

 





