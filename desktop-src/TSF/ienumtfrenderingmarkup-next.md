---
title: Método Next IEnumTfRenderingMarkup
description: El siguiente método IEnumTfRenderingMarkup obtiene, desde la posición actual, el número especificado de elementos de la secuencia de enumeración.
ms.assetid: a3aec919-2c65-4e65-9430-d73fdaf5d28e
keywords:
- Next Method Text Services Framework
- Next Method Text Services Framework, IEnumTfRenderingMarkup (interfaz)
- IEnumTfRenderingMarkup interface Text Services Framework, Next (método)
topic_type:
- apiref
api_name:
- IEnumTfRenderingMarkup.Next
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 0989d35a2fa7c521d5ea103fbe40a73d012a3997
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104078001"
---
# <a name="ienumtfrenderingmarkupnext-method"></a>IEnumTfRenderingMarkup:: Next (método)

El método **IEnumTfRenderingMarkup:: Next** obtiene, desde la posición actual, el número especificado de elementos de la secuencia de enumeración.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT Next(
  [out] ULONG ulCount,
  [out]       ppElement,
  [out] ULONG *pcFetched
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*ulCount* \[ enuncia\]
</dt> <dd>

\[out \] especifica el número de elementos que se van a obtener.

</dd> <dt>

*ppElement* \[ enuncia\]
</dt> <dd>

\[out \] puntero a una matriz de [estructuras \_ RENDERINGMARKUP de TF](/windows/desktop/TSF/tf-renderingmarkup) . Esta matriz debe tener al menos *ulCount* elementos de tamaño.

</dd> <dt>

*pcFetched* \[ enuncia\]
</dt> <dd>

\[out \] puntero a un valor ulong que recibe el número de elementos obtenidos realmente. Este valor puede ser menor que el número de elementos solicitados. Este parámetro puede ser **NULL**.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método puede devolver uno de estos valores.



| Value                                                                                        | Descripción                                                                                                         |
|----------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ correcto**</dt> </dl>         | Método realizado correctamente.<br/>                                                                               |
| <dl> <dt>**S \_ false**</dt> </dl>      | El método llegó al final de la enumeración antes de que se pudiera obtener el número especificado de elementos.<br/> |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl> | Uno o más parámetros no son válidos.<br/>                                                                      |



 

## <a name="remarks"></a>Observaciones

> [!Note]  
> Este método no está actualmente en los archivos de encabezado públicos. Para usar esta API, debe compilar MIDL en el [prototipo](prototypes.md).

 

 

