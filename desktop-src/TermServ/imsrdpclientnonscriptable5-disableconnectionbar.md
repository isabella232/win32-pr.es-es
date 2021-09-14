---
title: Propiedad DisableConnectionBar de IMsRdpClientNonScriptable5
description: Especifica si el control Escritorio remoto ActiveX debe deshabilitar la barra de conexión.
ms.assetid: 82c57b93-f976-43e6-97f9-3602bf97e466
ms.tgt_platform: multiple
keywords:
- Propiedad DisableConnectionBar Servicios de Escritorio remoto
- Propiedad DisableConnectionBar Servicios de Escritorio remoto , interfaz IMsRdpClientNonScriptable5
- Interfaz IMsRdpClientNonScriptable5 Servicios de Escritorio remoto , propiedad DisableConnectionBar
topic_type:
- apiref
api_name:
- IMsRdpClientNonScriptable5.DisableConnectionBar
- IMsRdpClientNonScriptable5.put_DisableConnectionBar
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a129d4781db69a564eecbca3a715c3c5ccf1a9cc
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127071030"
---
# <a name="imsrdpclientnonscriptable5disableconnectionbar-property"></a>IMsRdpClientNonScriptable5::D isableConnectionBar

Especifica si el control Escritorio remoto ActiveX debe deshabilitar la barra de conexión. Si esta propiedad contiene **VARIANT \_ TRUE**, se debe deshabilitar la barra de conexión. Si esta propiedad contiene **VARIANT \_ FALSE**, la barra de conexión debe estar habilitada.

Esta propiedad es de solo escritura.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT put_DisableConnectionBar(
  [in] VARIANT_BOOL fDisableConnectionBar
);
```



## <a name="property-value"></a>Valor de propiedad

Especifica el nuevo valor de propiedad.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 7<br/>                                                                          |
| Servidor mínimo compatible<br/> | Windows Server 2008 R2<br/>                                                             |
| Biblioteca de tipos<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>        |
| Archivo DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>        |
| IID<br/>                      | IID \_ IMsRdpClientNonScriptable5 se define como 4f6996d5-d7b1-412c-b0ff-063718566907<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IMsRdpClientNonScriptable5**](imsrdpclientnonscriptable5.md)
</dt> </dl>

 

 





