---
description: Representa información sobre el historial de píxeles.
MS-HAID: vspixengine.PixelHistoryOperation
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Estructura PixelHistoryOperation
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 59DC72FC-3865-48D3-9F92-9BE93DCA093B
api_name:
- PixelHistoryOperation
api_type:
- HeaderDef
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: c02a6725f588aaa4c7d72c48d03d921503d4e6a6
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "105705219"
---
# <a name="span-idvspixenginepixelhistoryoperationspanpixelhistoryoperation-structure"></a><span id="vspixengine.pixelhistoryoperation"></span>Estructura PixelHistoryOperation

Representa información sobre el historial de píxeles.

## <a name="syntax"></a>Sintaxis


```C++
} PixelHistoryOperation;
```

## <a name="members"></a>Miembros

**Eid**  
IDENTIFICADOR del evento de gráficos asociado a esta operación.

**MEDICO**  
Llamadas empaquetadas asociadas a esta operación.

**renderTargetPtr**  
Destino de representación asociado originalmente (dentro de la aplicación capturada) con esta operación.

**iPrim**  
Índice del primitivo real asociado a su operación.

**numPrims**  
Número total de primitivas asociadas a esta operación.

**numVertsPerPrim**  
El número de vértices por primitivo.

**iInstance**  
Al representar instancias, el número de instancia de la instancia real asociada a esta operación.

**iInstanceCount**  
Al representar las instancias, el número total de instancias asociadas a esta operación.

**bAssemblerStageGeneratesInstanceID**  
True si el ensamblador de entrada genera identificadores de instancia; en caso contrario, false.

**flags**  
Combinación de valores de PIXELHISTORYFLAGS. Para obtener más información, consulte la enumeración PIXELHISTORYFLAGS.

**pVSFile**  
Un FILEPTR para la secuencia de bytes del sombreador de píxeles. Esto se devuelve para depurar.

**pGSFile**  
FILEPTR para el flujo de bytes del sombreador de geometría. Esto se devuelve para depurar.

**pPSFile**  
Un FILEPTR para la secuencia de bytes del sombreador de píxeles. Esto se devuelve para depurar.

**pHSFile**  
Un FILEPTR para la secuencia de bytes del sombreador de casco. Esto se devuelve para depurar.

**pDSFile**  
FILEPTR para el flujo de bytes del sombreador de dominio. Esto se devuelve para depurar.

**pCSFile**  
Un FILEPTR para la secuencia de bytes del sombreador de cálculo. Esto se devuelve para depurar.

**VertexShaderFile**  
Cadena COM que contiene la ruta de acceso del archivo de origen del sombreador de vértices.

**PixelShaderFile**  
Cadena COM que contiene la ruta de acceso del archivo de origen del sombreador de píxeles.

**GeometryShaderFile**  
Cadena COM que contiene la ruta de acceso del archivo de origen del sombreador de geometría.

**HullShaderFile**  
Cadena COM que contiene la ruta de acceso del archivo de origen del sombreador de casco.

**DomainShaderFile**  
Cadena COM que contiene la ruta de acceso del archivo de origen del sombreador de dominios.

**psRed**  
Salida del sombreador de píxeles: valor del componente de color rojo.

**psGreen**  
Salida del sombreador de píxeles: valor del componente de color verde.

**psBlue**  
Salida del sombreador de píxeles: valor de componente de color azul

**psAlpha**  
Salida del sombreador de píxeles: valor del componente de color alfa

**LabelPSRed**  
Cadena COM que contiene el nombre de la etiqueta asociada al componente de color rojo de la salida del sombreador de píxeles.

**LabelPSGreen**  
Cadena COM que contiene el nombre de la etiqueta asociada al componente de color verde de la salida del sombreador de píxeles.

**LabelPSBlue**  
Cadena COM que contiene el nombre de la etiqueta asociada al componente de color azul de la salida del sombreador de píxeles.

**LabelPSAlpha**  
Cadena COM que contiene el nombre de la etiqueta asociada al componente de color alfa de la salida del sombreador de píxeles.

**pixelKillReason**  
Salida del sombreador de píxeles: motivo por el que se eliminó la salida del píxel.

**pixelOccluded**  
True si el píxel es ocluidos; en caso contrario, false.

**fbRed**  
Fotogramas: valor del componente de color rojo de fotogramas antes de que se combine el resultado del sombreador de píxeles.

**fbGreen**  
Fotogramas: valor del componente de color verde de fotogramas antes de que se combine el resultado del sombreador de píxeles.

**fbBlue**  
Fotogramas: valor del componente de color azul de fotogramas antes de que se combine el resultado del sombreador de píxeles.

**fbAlpha**  
Fotogramas: valor del componente de color alfa de fotogramas antes de que se combine el resultado del sombreador de píxeles.

**LabelFBRed**  
Cadena COM que contiene el nombre de la etiqueta asociada al componente de color rojo del fotogramas.

**LabelFBGreen**  
Cadena COM que contiene el nombre de la etiqueta asociada al componente de color verde del fotogramas.

**LabelFBBlue**  
Cadena COM que contiene el nombre de la etiqueta asociada al componente de color azul del fotogramas.

**LabelFBAlpha**  
Cadena COM que contiene el nombre de la etiqueta asociada al componente de color alfa del fotogramas.

**topología**  
La topología de vértices de las llamadas a Draw (lista de triángulos, franja de triángulo, etc.).

**vértices**  
Cadena COM que contiene el búfer de vértices a partir de este primitivo. El búfer de vértices sigue el formato de diseño de entrada especificado en la fase de canalización.

**vertexSize**  
Tamaño de un único vértice en bytes.

**InputLayout**  
Cadena COM que contiene una secuencia de estructuras InputLayoutStruct asociadas a la llamada a Draw.

**HResult**  
HRESULT de DirectX. En caso de que se produce un problema, se puede usar para mostrar el error.

## <a name="requirements"></a>Requisitos

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p>Encabezado</p></td><td>Vspixengine. h</td></tr></tbody></table>

 

 



