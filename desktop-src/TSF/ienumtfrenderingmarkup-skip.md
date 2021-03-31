---
title: IEnumTfRenderingMarkup SKIP (método)
description: El método SKIP de IEnumTfRenderingMarkup obtiene, desde la posición actual, el número especificado de elementos de la secuencia de enumeración.
ms.assetid: d328dfe3-36ab-4daf-8809-ad6686ca5dae
keywords:
- Skip Method Text Services Framework
- Skip Method Text Services Framework, IEnumTfRenderingMarkup (interfaz)
- IEnumTfRenderingMarkup interface Text Services Framework, SKIP (método)
topic_type:
- apiref
api_name:
- IEnumTfRenderingMarkup.Skip
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 3542893c739e6cfa2933d95bfed31f16957a0841
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/25/2019
ms.locfileid: "103783707"
---
# <a name="ienumtfrenderingmarkupskip-method"></a>IEnumTfRenderingMarkup:: Skip (método)

El método **IEnumTfRenderingMarkup:: Skip** obtiene, desde la posición actual, el número especificado de elementos de la secuencia de enumeración.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT Skip(
  [in] ULONG ulCount
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*ulCount* \[ de\]
</dt> <dd>

\[en \] especifica el número de elementos que se van a omitir.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método puede devolver uno de estos valores.



| Value                                                                                   | Descripción                                                                                                        |
|-----------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ correcto**</dt> </dl>    | Método realizado correctamente.<br/>                                                                              |
| <dl> <dt>**S \_ false**</dt> </dl> | El método llegó al final de la enumeración antes de que se pudiera omitir el número especificado de elementos.<br/> |



 

## <a name="remarks"></a>Observaciones

> [!Note]  
> Este método no está actualmente en los archivos de encabezado públicos. Para usar esta API, debe compilar MIDL en el [prototipo](prototypes.md).

 

 

 





