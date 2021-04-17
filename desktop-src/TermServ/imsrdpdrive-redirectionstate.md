---
title: Propiedad RedirectionState de IMsRdpDrive
description: Indica el estado de redireccionamiento de la unidad.
ms.assetid: 05333671-460d-4c07-8b7e-fbb7bc215353
ms.tgt_platform: multiple
keywords:
- Servicios de Escritorio remoto de la propiedad RedirectionState
- Propiedad RedirectionState Servicios de Escritorio remoto, interfaz IMsRdpDrive
- Servicios de Escritorio remoto de la interfaz IMsRdpDrive, propiedad RedirectionState
topic_type:
- apiref
api_name:
- IMsRdpDrive.RedirectionState
- IMsRdpDrive.get_RedirectionState
- IMsRdpDrive.put_RedirectionState
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7561190e976e0b8190553376f5e9f7a5b2de2550
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104422476"
---
# <a name="imsrdpdriveredirectionstate-property"></a>IMsRdpDrive:: RedirectionState (propiedad)

Indica el estado de redireccionamiento de la unidad.

Esta propiedad es de lectura y escritura.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT put_RedirectionState(
  [in]  VARIANT_BOOL vboolRedirState
);

HRESULT get_RedirectionState(
  [out] VARIANT_BOOL *pvboolRedirState
);
```



## <a name="property-value"></a>Valor de propiedad

Establezca este parámetro en **Variant \_ false**. para deshabilitar la redirección o la **variante \_ verdadera**. para habilitar la redirección.

## <a name="error-codes"></a>Códigos de error

Si el método se ejecuta correctamente, se devuelve **S \_ OK** . Cualquier otro valor **HRESULT** indica que se produjo un error en la llamada.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                               |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                         |
| Biblioteca de tipos<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl> |
| IID<br/>                      | IID \_ IMsRdpDrive se define como d28b5458-f694-47a8-8e61-40356a767e46<br/>         |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IMsRdpDrive**](imsrdpdrive.md)
</dt> </dl>

 

 





