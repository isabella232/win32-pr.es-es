---
title: IEnumTfRenderingMarkup Clone (método)
description: El método Clone IEnumTfRenderingMarkup crea una copia del objeto de enumerador.
ms.assetid: f1b0ccf9-36d1-4eff-af7c-d7fb4f0e9104
keywords:
- Método Clone Text Services Framework
- Clone Method Text Services Framework, IEnumTfRenderingMarkup (interfaz)
- IEnumTfRenderingMarkup interface Text Services Framework, Clone (método)
topic_type:
- apiref
api_name:
- IEnumTfRenderingMarkup.Clone
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 7f15d1bda18d2371f6518da4fa2884fac4df91b4
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "105685738"
---
# <a name="ienumtfrenderingmarkupclone-method"></a>IEnumTfRenderingMarkup:: Clone (método)

El método **IEnumTfRenderingMarkup:: Clone** crea una copia del objeto de enumerador.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT Clone(
  [out] IEnumTfRenderingMarkup **ppEnum
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*ppEnum* \[ enuncia\]
</dt> <dd>

\[\]un puntero a una interfaz [IEnumTfRenderingMarkup](/windows/desktop/TSF/ienumtfrenderingmarkup) .

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método puede devolver uno de estos valores.



| Value                                                                                        | Descripción                                    |
|----------------------------------------------------------------------------------------------|------------------------------------------------|
| <dl> <dt>**S \_ correcto**</dt> </dl>         | Método realizado correctamente.<br/>          |
| <dl> <dt>**E \_ FAIL**</dt> </dl>       | Se ha producido un error no especificado.<br/>      |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl> | Uno o más parámetros no son válidos.<br/> |



 

## <a name="remarks"></a>Observaciones

> [!Note]  
> Este método no está actualmente en los archivos de encabezado públicos. Para usar esta API, debe compilar MIDL en el [prototipo](prototypes.md).

 

 

