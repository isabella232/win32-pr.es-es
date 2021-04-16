---
description: Libera un \_ contexto de cadena PCCERT \_ adquirido a través de la propiedad ChainContext.
ms.assetid: fa9a6171-58ff-400f-bdcc-ba32a0ae0441
title: 'IChainContext:: FreeContext (método)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IChainContext.FreeContext
- ChainContext.FreeContext
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 413b119f250bfbd061301391fee7741362979f65
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690521"
---
# <a name="ichaincontextfreecontext-method"></a>IChainContext:: FreeContext (método)

\[CAPICOM es un componente de solo bits de 32 que está disponible para su uso en los siguientes sistemas operativos: Windows Server 2008, Windows Vista y Windows XP.\]

El método **FreeContext** libera un \_ contexto de cadena PCCERT \_ adquirido a través de la propiedad [**ChainContext**](ichaincontext-chaincontext.md) .

## <a name="syntax"></a>Sintaxis


```VB
ChainContext.FreeContext()
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pChainContext* \[ de\]
</dt> <dd>

Contexto de la \_ cadena \_ de PCCERT que se va a liberar.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

El valor devuelto es **HRESULT**. Un valor de S \_ OK indica que se ha realizado correctamente. Cualquier otro valor indica que se produjo un error en la operación.

## <a name="remarks"></a>Observaciones

Este método no libera el contexto de la \_ cadena PCCERT \_ contenido dentro de un objeto de [**cadena**](chain.md) . Solo se debe usar para liberar un contexto de \_ cadena de PCCERT \_ adquirido a través de la propiedad [**ChainContext**](ichaincontext-chaincontext.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|----------------------------|----------------------------------------------------------------------------------------|
| Redistribuible<br/> | CAPICOM 2,0 o posterior en Windows Server 2003 y Windows XP<br/>                  |
| Archivo DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IChainContext**](ichaincontext.md)
</dt> </dl>

 

 




