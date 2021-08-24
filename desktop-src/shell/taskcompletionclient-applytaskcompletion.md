---
description: Comienza la finalización de la tarea.
ms.assetid: 75C84DD9-D815-45C2-A28E-EAE437EAFF89
title: Método TaskCompletionClient::ApplyTaskCompletion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- TaskCompletionClient.ApplyTaskCompletion
api_type:
- COM
api_location:
- ExecModelClient.dll
ms.openlocfilehash: 58c95144077697f1655547a58571ce3475355aa96040ce1815bd3178bc9a1290
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119773675"
---
# <a name="taskcompletionclientapplytaskcompletion-method"></a>Método TaskCompletionClient::ApplyTaskCompletion

Comienza la finalización de la tarea.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT ApplyTaskCompletion(
    UINT32   ptcfCategory
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*ptcfCategory* 
</dt> <dd>

Valor que indica la categoría de la tarea.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si este método se realiza correctamente, devuelve **S \_ OK**. De lo contrario, devuelve un código de error **HRESULT.**

## <a name="remarks"></a>Comentarios

El único valor admitido para *ptcfCategory* es 0x08000000.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Windows 10 solo aplicaciones de escritorio\]<br/>                                                    |
| Servidor mínimo compatible<br/> | \[Windows Server 2016 solo aplicaciones de escritorio\]<br/>                                           |
| Archivo DLL<br/>                      | <dl> <dt>ExecModelClient.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**TaskCompletionClient**](taskcompletionclient.md)
</dt> </dl>

 

 




