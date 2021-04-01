---
title: Propiedad RemoteMonitorLayoutMatchesLocal de IMsRdpClientNonScriptable5
description: Especifica si el diseño del monitor remoto es idéntico al diseño del monitor local.
ms.assetid: 8F3C6650-870C-417C-82FC-E145FC360012
ms.tgt_platform: multiple
keywords:
- Servicios de Escritorio remoto de la propiedad RemoteMonitorLayoutMatchesLocal
- Propiedad RemoteMonitorLayoutMatchesLocal Servicios de Escritorio remoto, interfaz IMsRdpClientNonScriptable5
- Servicios de Escritorio remoto de la interfaz IMsRdpClientNonScriptable5, propiedad RemoteMonitorLayoutMatchesLocal
topic_type:
- apiref
api_name:
- IMsRdpClientNonScriptable5.RemoteMonitorLayoutMatchesLocal
- IMsRdpClientNonScriptable5.get_RemoteMonitorLayoutMatchesLocal
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c5018b22865cc683fc9231c857a1b99b8acbfeca
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150599"
---
# <a name="imsrdpclientnonscriptable5remotemonitorlayoutmatcheslocal-property"></a>IMsRdpClientNonScriptable5:: RemoteMonitorLayoutMatchesLocal (propiedad)

Especifica si el diseño del monitor remoto es idéntico al diseño del monitor local. Si esta propiedad contiene **Variant \_ true**, el diseño del monitor remoto es idéntico al diseño del monitor local. Si esta propiedad contiene **Variant \_ false**, los monitores remotos y locales tienen diseños diferentes.

Esta propiedad es de solo lectura.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT get_RemoteMonitorLayoutMatchesLocal(
  [out, retval] VARIANT_BOOL *pfRemoteMatchesLocal
);
```



## <a name="property-value"></a>Valor de propiedad

Recibe el valor de la propiedad.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 7<br/>                                                                          |
| Servidor mínimo compatible<br/> | Windows Server 2008 R2<br/>                                                             |
| Biblioteca de tipos<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>        |
| Archivo DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>        |
| IID<br/>                      | IID \_ IMsRdpClientNonScriptable5 se define como 4f6996d5-d7b1-412C-b0ff-063718566907<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IMsRdpClientNonScriptable5**](imsrdpclientnonscriptable5.md)
</dt> </dl>

 

 





