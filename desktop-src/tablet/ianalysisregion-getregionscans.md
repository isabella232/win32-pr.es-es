---
description: Recupera una matriz de rectángulos que define el área de IAnalysisRegion.
ms.assetid: 40de4c27-4b3b-4db3-af08-cb53e638db6b
title: Método IAnalysisRegion::GetRegionScans (IACom.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAnalysisRegion.GetRegionScans
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: e197126a99023fb96c2798343b391d53de4f6cd97aaaa141918f0fe705e5ad1e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118045322"
---
# <a name="ianalysisregiongetregionscans-method"></a>IAnalysisRegion::GetRegionScans (método)

Recupera una matriz de rectángulos que define el área de [**IAnalysisRegion**](ianalysisregion.md).

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetRegionScans(
  [out] ULONG *pulCount,
  [out] RECT  **pRegionScans
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pulCount* \[ out\]
</dt> <dd>

Número de rectángulos devueltos en *pRegionScans.*

</dd> <dt>

*pRegionScans* \[ out\]
</dt> <dd>

Puntero a una matriz de rectángulos que define el área de [**IAnalysisRegion**](ianalysisregion.md).

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Para obtener una descripción de los valores [devueltos, vea Clases e interfaces: análisis de entrada de lápiz.](classes-and-interfaces---ink-analysis.md)

## <a name="remarks"></a>Comentarios

Si *pRegionScans se* pasa como **NULL,** el **método GetRegionScans** devuelve S **\_ OK** y el número de rectángulos se devuelve en *pulCount.*

> [!Caution]  
> Para evitar una pérdida de memoria, use [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree) para liberar la memoria de \* *pRegionScans* cuando ya no necesite la información.

 

Los límites de los rectángulos están en coordenadas de espacio de entrada de lápiz.

La unión de los rectángulos devueltos representa el área de [**IAnalysisRegion**](ianalysisregion.md).

## <a name="examples"></a>Ejemplos

En el ejemplo siguiente se muestra cómo obtener los rectángulos que definen el área de [**IAnalysisRegion**](ianalysisregion.md)y cómo obtener `region` solo el número de rectángulos.


```C++
// Get the count and the rectangles.
ULONG count = 0;
RECT* rects = 0;
region->GetRegionScans(&count, &rects);

// Use rects

::CoTaskMemFree(rects);

// GetRegionScans just gets the count and returns S_OK
ULONG number = 0;
region->GetRegionScans(&number, NULL); 
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de XP Tablet PC \[ Edition\]<br/>                                                 |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                                                     |
| Header<br/>                   | <dl> <dt>IACom.h (también requiere IACom \_ i.c)</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>IACom.dll</dt> </dl>                          |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IAnalysisRegion**](ianalysisregion.md)
</dt> <dt>

[**IAnalysisRegion::GetBounds (Método)**](ianalysisregion-getbounds.md)
</dt> <dt>

[Referencia de análisis de entrada de lápiz](ink-analysis-reference.md)
</dt> </dl>

 

