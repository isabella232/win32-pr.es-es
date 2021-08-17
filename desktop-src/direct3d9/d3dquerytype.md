---
description: Identifica el tipo de consulta.
ms.assetid: 575c4e71-3cab-4123-a2a5-d23b53e87111
title: Enumeración D3DQUERYTYPE (D3D9Types.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DQUERYTYPE
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: b60f6a52f782efee8647828509e04b99a2ffd94489b9db215158090497947229
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117732326"
---
# <a name="d3dquerytype-enumeration"></a>D3DQUERYTYPE (enumeración)

Identifica el tipo de consulta. Para obtener información sobre las consultas, vea [Consultas (Direct3D 9)](queries.md)

## <a name="syntax"></a>Syntax


```C++
typedef enum D3DQUERYTYPE { 
  D3DQUERYTYPE_VCACHE             = 4,
  D3DQUERYTYPE_RESOURCEMANAGER    = 5,
  D3DQUERYTYPE_VERTEXSTATS        = 6,
  D3DQUERYTYPE_EVENT              = 8,
  D3DQUERYTYPE_OCCLUSION          = 9,
  D3DQUERYTYPE_TIMESTAMP          = 10,
  D3DQUERYTYPE_TIMESTAMPDISJOINT  = 11,
  D3DQUERYTYPE_TIMESTAMPFREQ      = 12,
  D3DQUERYTYPE_PIPELINETIMINGS    = 13,
  D3DQUERYTYPE_INTERFACETIMINGS   = 14,
  D3DQUERYTYPE_VERTEXTIMINGS      = 15,
  D3DQUERYTYPE_PIXELTIMINGS       = 16,
  D3DQUERYTYPE_BANDWIDTHTIMINGS   = 17,
  D3DQUERYTYPE_CACHEUTILIZATION   = 18,
  D3DQUERYTYPE_MEMORYPRESSURE     = 19
} D3DQUERYTYPE, *LPD3DQUERYTYPE;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="D3DQUERYTYPE_VCACHE"></span><span id="d3dquerytype_vcache"></span>**D3DQUERYTYPE \_ VCACHE**
</dt> <dd>

Consulta de sugerencias de controlador sobre el diseño de datos para el almacenamiento en caché de vértices.

</dd> <dt>

<span id="D3DQUERYTYPE_ResourceManager"></span><span id="d3dquerytype_resourcemanager"></span><span id="D3DQUERYTYPE_RESOURCEMANAGER"></span>**D3DQUERYTYPE \_ ResourceManager**
</dt> <dd>

Consulte el administrador de recursos. Para esta consulta, las marcas de comportamiento del dispositivo deben incluir [D3DCREATE \_ DISABLE \_ DRIVER \_ MANAGEMENT](d3dcreate.md).

</dd> <dt>

<span id="D3DQUERYTYPE_VERTEXSTATS"></span><span id="d3dquerytype_vertexstats"></span>**D3DQUERYTYPE \_ VERTEXSTATS**
</dt> <dd>

Consulta de estadísticas de vértices.

</dd> <dt>

<span id="D3DQUERYTYPE_EVENT"></span><span id="d3dquerytype_event"></span>**EVENTO D3DQUERYTYPE \_**
</dt> <dd>

Consulte todos y cada uno de los eventos asincrónicos emitidos desde llamadas API.

</dd> <dt>

<span id="D3DQUERYTYPE_OCCLUSION"></span><span id="d3dquerytype_occlusion"></span>**OCLUSIÓN DE D3DQUERYTYPE \_**
</dt> <dd>

Una consulta de oclusión devuelve el número de píxeles que pasan las pruebas z. Estos píxeles son para los primitivos dibujados entre el problema [**de D3DISSUE \_ BEGIN**](d3dissue-begin.md) y [**D3DISSUE \_ END.**](d3dissue-end.md) Esto permite a una aplicación comprobar el resultado de la oclusión en 0. Cero está totalmente ocluido, lo que significa que los píxeles no son visibles desde la posición actual de la cámara.

</dd> <dt>

<span id="D3DQUERYTYPE_TIMESTAMP"></span><span id="d3dquerytype_timestamp"></span>**MARCA DE TIEMPO D3DQUERYTYPE \_**
</dt> <dd>

Devuelve una marca de tiempo de 64 bits.

</dd> <dt>

<span id="D3DQUERYTYPE_TIMESTAMPDISJOINT"></span><span id="d3dquerytype_timestampdisjoint"></span>**D3DQUERYTYPE \_ TIMESTAMPDISJOINT**
</dt> <dd>

Use esta consulta para notificar a una aplicación si la frecuencia del contador ha cambiado con respecto a la marca de tiempo D3DQUERYTYPE. \_

</dd> <dt>

<span id="D3DQUERYTYPE_TIMESTAMPFREQ"></span><span id="d3dquerytype_timestampfreq"></span>**D3DQUERYTYPE \_ TIMESTAMPFREQ**
</dt> <dd>

Este resultado de consulta es **TRUE** si no se puede garantizar que los valores de las consultas TIMESTAMP de D3DQUERYTYPE sean continuos a lo largo de la duración de la consulta \_ D3DQUERYTYPE \_ TIMESTAMPDISJOINT. De lo contrario, el resultado de la **consulta es FALSE.**

</dd> <dt>

<span id="D3DQUERYTYPE_PIPELINETIMINGS"></span><span id="d3dquerytype_pipelinetimings"></span>**D3DQUERYTYPE \_ PIPELINETIMINGS**
</dt> <dd>

Porcentaje de tiempo de procesamiento de datos de canalización.

</dd> <dt>

<span id="D3DQUERYTYPE_INTERFACETIMINGS"></span><span id="d3dquerytype_interfacetimings"></span>**INTERFAZ \_ D3DQUERYTYPETIMINGS**
</dt> <dd>

Porcentaje de tiempo de procesamiento de datos en el controlador.

</dd> <dt>

<span id="D3DQUERYTYPE_VERTEXTIMINGS"></span><span id="d3dquerytype_vertextimings"></span>**VÉRTICES \_ D3DQUERYTYPETIMINGS**
</dt> <dd>

Porcentaje de tiempo de procesamiento de datos del sombreador de vértices.

</dd> <dt>

<span id="D3DQUERYTYPE_PIXELTIMINGS"></span><span id="d3dquerytype_pixeltimings"></span>**D3DQUERYTYPE \_ PIXELTIMINGS**
</dt> <dd>

Porcentaje de tiempo de procesamiento de datos del sombreador de píxeles.

</dd> <dt>

<span id="D3DQUERYTYPE_BANDWIDTHTIMINGS"></span><span id="d3dquerytype_bandwidthtimings"></span>**D3DQUERYTYPE \_ BANDWIDTHTIMINGS**
</dt> <dd>

Comparaciones de medidas de rendimiento para ayudar a comprender el rendimiento de una aplicación.

</dd> <dt>

<span id="D3DQUERYTYPE_CACHEUTILIZATION"></span><span id="d3dquerytype_cacheutilization"></span>**D3DQUERYTYPE \_ CACHEUTILIZATION**
</dt> <dd>

Mida el rendimiento de la tasa de aciertos de caché para texturas y vértices indexados.

</dd> <dt>

<span id="D3DQUERYTYPE_MEMORYPRESSURE"></span><span id="d3dquerytype_memorypressure"></span>**D3DQUERYTYPE \_ MEMORYPRESSURE**
</dt> <dd>

Eficiencia de la asignación de memoria contenida en una [**estructura D3DMEMORYPRESSURE.**](d3dmemorypressure.md)

Diferencias entre Direct3D 9 y Direct3D 9Ex:

- D3DQUERYTYPE MEMORYPRESSURE solo está disponible en Direct3D9Ex que se ejecuta \_ Windows 7 (o más sistema operativo actual).



 

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>D3D9Types.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Enumeraciones de Direct3D](dx9-graphics-reference-d3d-enums.md)
</dt> <dt>

[**IDirect3DDevice9::CreateQuery**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createquery)
</dt> </dl>

 

 
