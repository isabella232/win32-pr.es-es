---
title: Propiedad IMsRdpDrive Name
description: Recupera el nombre de la unidad.
ms.assetid: 5aabb7df-fd46-48aa-ad1d-51da45495782
ms.tgt_platform: multiple
keywords:
- Nombre de propiedad Servicios de Escritorio remoto
- Nombre de la Servicios de Escritorio remoto , interfaz IMsRdpDrive
- Interfaz IMsRdpDrive Servicios de Escritorio remoto , propiedad Name
topic_type:
- apiref
api_name:
- IMsRdpDrive.Name
- IMsRdpDrive.get_Name
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bde69814f38c39315a02a76bd52b8c3c38baffc2c0a92601ef383cb60b0bc492
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120125645"
---
# <a name="imsrdpdrivename-property"></a>Propiedad IMsRdpDrive::Name

Recupera el nombre de la unidad.

Esta propiedad es de solo lectura.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT get_Name(
  [out] BSTR *pName
);
```



## <a name="property-value"></a>Valor de propiedad

Nombre de la unidad.

## <a name="error-codes"></a>Códigos de error

Si el método se realiza correctamente, **se devuelve S \_ OK.** Cualquier otro **valor HRESULT** indica que se ha dado error en la llamada.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                               |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                         |
| Biblioteca de tipos<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl> |
| IID<br/>                      | IID IMsRdpDrive se define como \_ d28b5458-f694-47a8-8e61-40356a767e46<br/>         |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IMsRdpDrive**](imsrdpdrive.md)
</dt> </dl>

 

 





