---
title: Propiedad MarkRdpSettingsSecure de IMsRdpClientNonScriptable4
description: Especifica si los valores de Protocolo de escritorio remoto (RDP) se marcan como seguros.
ms.assetid: 04b419ed-821e-43e0-ac76-b8d6f6dfcc30
ms.tgt_platform: multiple
keywords:
- Servicios de Escritorio remoto de la propiedad MarkRdpSettingsSecure
- Propiedad MarkRdpSettingsSecure Servicios de Escritorio remoto, interfaz IMsRdpClientNonScriptable4
- Servicios de Escritorio remoto de la interfaz IMsRdpClientNonScriptable4, propiedad MarkRdpSettingsSecure
- Propiedad MarkRdpSettingsSecure Servicios de Escritorio remoto, interfaz IMsRdpClientNonScriptable5
- Servicios de Escritorio remoto de la interfaz IMsRdpClientNonScriptable5, propiedad MarkRdpSettingsSecure
- Servicios de Escritorio remoto de la propiedad MarkRdpSettingsSecure, objeto MsRdpClient6
- Servicios de Escritorio remoto de objeto MsRdpClient6, propiedad MarkRdpSettingsSecure
- Servicios de Escritorio remoto de la propiedad MarkRdpSettingsSecure, objeto MsRdpClient7
- Servicios de Escritorio remoto de objeto MsRdpClient7, propiedad MarkRdpSettingsSecure
- Servicios de Escritorio remoto de la propiedad MarkRdpSettingsSecure, objeto MsRdpClient8
- Servicios de Escritorio remoto de objeto MsRdpClient8, propiedad MarkRdpSettingsSecure
- Servicios de Escritorio remoto de la propiedad MarkRdpSettingsSecure, objeto MsRdpClient9
- Servicios de Escritorio remoto de objeto MsRdpClient9, propiedad MarkRdpSettingsSecure
topic_type:
- apiref
api_name:
- IMsRdpClientNonScriptable4.MarkRdpSettingsSecure
- IMsRdpClientNonScriptable4.get_MarkRdpSettingsSecure
- IMsRdpClientNonScriptable4.put_MarkRdpSettingsSecure
- IMsRdpClientNonScriptable5.MarkRdpSettingsSecure
- IMsRdpClientNonScriptable5.get_MarkRdpSettingsSecure
- IMsRdpClientNonScriptable5.put_MarkRdpSettingsSecure
- MsRdpClient6.MarkRdpSettingsSecure
- MsRdpClient7.MarkRdpSettingsSecure
- MsRdpClient8.MarkRdpSettingsSecure
- MsRdpClient9.MarkRdpSettingsSecure
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: df0b551e043432b6f6e66efbbe5a6e0f9095024a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104534450"
---
# <a name="imsrdpclientnonscriptable4markrdpsettingssecure-property"></a>IMsRdpClientNonScriptable4:: MarkRdpSettingsSecure (propiedad)

Especifica si los valores de [Protocolo de escritorio remoto](remote-desktop-protocol.md) (RDP) se marcan como seguros. Esto indica que los valores aplicados al control están firmados por un editor de terceros o de confianza.

Esta propiedad es de lectura y escritura.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT put_MarkRdpSettingsSecure(
  [in]  VARIANT_BOOL fRdpSecure
);

HRESULT get_MarkRdpSettingsSecure(
  [out] VARIANT_BOOL *pfRdpSecure
);
```



## <a name="property-value"></a>Valor de propiedad

Establece si la configuración de RDP está marcada como segura.

## <a name="error-codes"></a>Códigos de error

Devuelve **S \_ correcto** si se realiza correctamente.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                                 |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                           |
| Biblioteca de tipos<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>   |
| Archivo DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>   |
| IID<br/>                      | IMsRdpClientNonScriptable4 se define como f50fa8aa-1c7d-4f59-b15c-a90cacae1fcb<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IMsRdpClientNonScriptable5**](imsrdpclientnonscriptable5.md)
</dt> <dt>

[**IMsRdpClientNonScriptable4**](imsrdpclientnonscriptable4.md)
</dt> </dl>

 

 





