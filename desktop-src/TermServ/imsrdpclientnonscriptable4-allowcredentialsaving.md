---
title: Propiedad AllowCredentialSaving de IMsRdpClientNonScriptable4
description: Especifica si el cuadro de diálogo credenciales muestra una casilla que permite guardar las credenciales.
ms.assetid: c5148ff0-0d7f-413d-b2a8-ff942668bee6
ms.tgt_platform: multiple
keywords:
- Servicios de Escritorio remoto de la propiedad AllowCredentialSaving
- Propiedad AllowCredentialSaving Servicios de Escritorio remoto, interfaz IMsRdpClientNonScriptable4
- Servicios de Escritorio remoto de la interfaz IMsRdpClientNonScriptable4, propiedad AllowCredentialSaving
- Propiedad AllowCredentialSaving Servicios de Escritorio remoto, interfaz IMsRdpClientNonScriptable5
- Servicios de Escritorio remoto de la interfaz IMsRdpClientNonScriptable5, propiedad AllowCredentialSaving
- Servicios de Escritorio remoto de la propiedad AllowCredentialSaving, objeto MsRdpClient6
- Servicios de Escritorio remoto de objeto MsRdpClient6, propiedad AllowCredentialSaving
- Servicios de Escritorio remoto de la propiedad AllowCredentialSaving, objeto MsRdpClient7
- Servicios de Escritorio remoto de objeto MsRdpClient7, propiedad AllowCredentialSaving
- Servicios de Escritorio remoto de la propiedad AllowCredentialSaving, objeto MsRdpClient8
- Servicios de Escritorio remoto de objeto MsRdpClient8, propiedad AllowCredentialSaving
- Servicios de Escritorio remoto de la propiedad AllowCredentialSaving, objeto MsRdpClient9
- Servicios de Escritorio remoto de objeto MsRdpClient9, propiedad AllowCredentialSaving
topic_type:
- apiref
api_name:
- IMsRdpClientNonScriptable4.AllowCredentialSaving
- IMsRdpClientNonScriptable4.get_AllowCredentialSaving
- IMsRdpClientNonScriptable4.put_AllowCredentialSaving
- IMsRdpClientNonScriptable5.AllowCredentialSaving
- IMsRdpClientNonScriptable5.get_AllowCredentialSaving
- IMsRdpClientNonScriptable5.put_AllowCredentialSaving
- MsRdpClient6.AllowCredentialSaving
- MsRdpClient7.AllowCredentialSaving
- MsRdpClient8.AllowCredentialSaving
- MsRdpClient9.AllowCredentialSaving
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 240e2eb8e80209ee5c90d63f2996231cf84bb2dc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105686030"
---
# <a name="imsrdpclientnonscriptable4allowcredentialsaving-property"></a>IMsRdpClientNonScriptable4:: AllowCredentialSaving (propiedad)

Especifica si el cuadro de diálogo credenciales muestra una casilla que permite guardar las credenciales.

Esta propiedad es de lectura y escritura.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT put_AllowCredentialSaving(
  [in]  VARIANT_BOOL fAllowSave
);

HRESULT get_AllowCredentialSaving(
  [out] VARIANT_BOOL *pfAllowSave
);
```



## <a name="property-value"></a>Valor de propiedad

Establece si el cuadro de diálogo credenciales muestra una casilla que permite guardar las credenciales.

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

 

 





