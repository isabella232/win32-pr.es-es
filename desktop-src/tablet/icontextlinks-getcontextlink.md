---
description: Recupera IContextLink en el índice especificado.
ms.assetid: 46bb71b9-5ef3-4756-97f6-40e0aaa82826
title: Método IContextLinks::GetContextLink (IACom.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextLinks.GetContextLink
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 01cf3b971b8533f21185a9b6e65c3cfb25109e657e2c9e2a931253d86c51dbdb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119940315"
---
# <a name="icontextlinksgetcontextlink-method"></a>IContextLinks::GetContextLink (método)

Recupera [**IContextLink en**](icontextlink.md) el índice especificado.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetContextLink(
  [in]  ULONG        ulIndex,
  [out] IContextLink **ppContextLink
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*ulIndex* \[ En\]
</dt> <dd>

Índice de base cero del objeto [**IContextLink**](icontextlink.md) que se obtiene.

</dd> <dt>

*ppContextLink* \[ out\]
</dt> <dd>

Puntero al objeto [**IContextLink**](icontextlink.md) en el índice especificado.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Para obtener una descripción de los valores [devueltos, vea Clases e interfaces: análisis de entrada de lápiz.](classes-and-interfaces---ink-analysis.md)

## <a name="remarks"></a>Comentarios

> [!Caution]  
> Para evitar una pérdida de memoria, llame a [**IUnknown::Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) en \* *ppContextLink* cuando ya no necesite usar el vínculo de contexto.

 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de XP Tablet PC \[ Edition\]<br/>                                                 |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                                                     |
| Header<br/>                   | <dl> <dt>IACom.h (también requiere IACom \_ i.c)</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>IACom.dll</dt> </dl>                          |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IContextLinks**](icontextlinks.md)
</dt> <dt>

[**IContextNode**](icontextnode.md)
</dt> <dt>

[Referencia de análisis de entrada de lápiz](ink-analysis-reference.md)
</dt> </dl>

 

