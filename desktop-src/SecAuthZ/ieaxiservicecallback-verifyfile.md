---
description: Realiza comprobaciones de seguridad en el objeto ActiveX especificado y devuelve la ubicación donde se descargó el .cab archivo correspondiente.
ms.assetid: ba8e4f9b-1569-43f9-b27c-a987044fff41
title: IeAxiServiceCallback::VerifyFile (método)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IeAxiServiceCallback.VerifyFile
api_type:
- COM
api_location: ''
ms.openlocfilehash: 6d590f5e0e7ecd881a51844737f8efddf34d6727
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127160823"
---
# <a name="ieaxiservicecallbackverifyfile-method"></a>IeAxiServiceCallback::VerifyFile (método)

El **método VerifyFile** realiza comprobaciones de seguridad en el objeto ActiveX especificado y devuelve la ubicación donde se descargó el archivo .cab correspondiente.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT VerifyFile(
  [in]  BSTR bstrFileUrl,
  [out] BSTR *bstrApprovedFileName
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*bstrFileUrl* \[ En\]
</dt> <dd>

Dirección URL del objeto ActiveX que se debe comprobar.

</dd> <dt>

*bstrApprovedFileName* \[ out\]
</dt> <dd>

Nombre del archivo donde se descargó .cab archivo asociado al ActiveX objeto.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si el método se realiza correctamente, el método devuelve S \_ OK.

Si se produce un error en el método , devuelve un **valor HRESULT** que indica el error. Para obtener una lista de códigos de error comunes, vea [Common HRESULT Values](/windows/desktop/SecCrypto/common-hresult-values).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista Business, Windows Vista Enterprise, Windows aplicaciones de escritorio de Vista \[ Ultimate\]<br/> |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                                                 |
| IID<br/>                      | IID IeAxiServiceCallback se define como \_ 1823E7BA-EC36-447a-9B2E-B4912E15AFE7<br/>                   |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**IeAxiServiceCallback**](ieaxiservicecallback.md)
</dt> </dl>

 

