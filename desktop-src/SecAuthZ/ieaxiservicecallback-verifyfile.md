---
description: Realiza comprobaciones de seguridad en el objeto ActiveX especificado y devuelve la ubicación donde se descargó el archivo. CAB correspondiente.
ms.assetid: ba8e4f9b-1569-43f9-b27c-a987044fff41
title: 'IeAxiServiceCallback:: VerifyFile (método)'
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
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104546531"
---
# <a name="ieaxiservicecallbackverifyfile-method"></a>IeAxiServiceCallback:: VerifyFile (método)

El método **VerifyFile** realiza comprobaciones de seguridad en el objeto ActiveX especificado y devuelve la ubicación donde se descargó el archivo. CAB correspondiente.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT VerifyFile(
  [in]  BSTR bstrFileUrl,
  [out] BSTR *bstrApprovedFileName
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*bstrFileUrl* \[ de\]
</dt> <dd>

Dirección URL del objeto ActiveX que se va a comprobar.

</dd> <dt>

*bstrApprovedFileName* \[ enuncia\]
</dt> <dd>

Nombre del archivo donde se descargó el archivo. cab asociado al objeto ActiveX.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si el método se ejecuta correctamente, el método devuelve S \_ correcto.

Si se produce un error en el método, devuelve un valor **HRESULT** que indica el error. Para obtener una lista de los códigos de error comunes, vea [Valores HRESULT comunes](/windows/desktop/SecCrypto/common-hresult-values).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista Business, Windows Vista Enterprise, Windows Vista Ultimate \[ solo aplicaciones de escritorio\]<br/> |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                                                 |
| IID<br/>                      | IID \_ IeAxiServiceCallback se define como 1823E7BA-EC36-447A-9B2E-B4912E15AFE7<br/>                   |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IeAxiServiceCallback**](ieaxiservicecallback.md)
</dt> </dl>

 

