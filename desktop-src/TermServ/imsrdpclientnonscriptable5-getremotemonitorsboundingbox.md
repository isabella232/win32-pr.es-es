---
title: Propiedad IMsRdpClientNonScriptable5 GetRemoteMonitorsBoundingBox
description: Especifica el rectángulo delimitador del monitor remoto.
ms.assetid: 4A8794F7-1DB4-4415-8538-6B2A365B22D3
ms.tgt_platform: multiple
keywords:
- Propiedad GetRemoteMonitorsBoundingBox Servicios de Escritorio remoto
- Propiedad GetRemoteMonitorsBoundingBox Servicios de Escritorio remoto , interfaz IMsRdpClientNonScriptable5
- Interfaz IMsRdpClientNonScriptable5 Servicios de Escritorio remoto , propiedad GetRemoteMonitorsBoundingBox
topic_type:
- apiref
api_name:
- IMsRdpClientNonScriptable5.GetRemoteMonitorsBoundingBox
- IMsRdpClientNonScriptable5.get_GetRemoteMonitorsBoundingBox
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 97f67192b78c734359fc6113969eb5eb410e1bf3
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127071023"
---
# <a name="imsrdpclientnonscriptable5getremotemonitorsboundingbox-property"></a>Propiedad IMsRdpClientNonScriptable5::GetRemoteMonitorsBoundingBox

Especifica el rectángulo delimitador del monitor remoto.

Esta propiedad es de solo lectura.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT get_GetRemoteMonitorsBoundingBox(
  [out] LONG *pLeft,
  [out] LONG *pTop,
  [out] LONG *pRight,
  [out] LONG *pBottom
);
```



## <a name="property-value"></a>Valor de propiedad

Recibe el borde izquierdo del rectángulo.

Recibe el borde superior del rectángulo.

Recibe el borde derecho del rectángulo.

Recibe el borde inferior del rectángulo.

## <a name="remarks"></a>Observaciones

Todas las coordenadas están en coordenadas de pantalla virtual, que son relativas a la esquina superior izquierda del monitor principal. Si este no es el monitor principal, algunos o todos estos valores pueden ser negativos.

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

 

 





