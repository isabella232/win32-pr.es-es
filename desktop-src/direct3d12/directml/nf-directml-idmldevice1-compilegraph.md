---
UID: NF:directml.IDMLDevice1.CompileGraph
title: IDMLDevice1::CompileGraph
description: Compila un grafo de operadores de DirectML en un objeto que se puede enviar a la GPU.
helpviewer_keywords:
- CompileGraph
- CompileGraph method
- CompileGraph method
- IDMLDevice1 interface
- IDMLDevice1 interface
- CompileGraph method
- IDMLDevice1.CompileGraph
- IDMLDevice1::CompileGraph
- direct3d12.idmldevice1_compileoperator
- directml/IDMLDevice1::CompileGraph
ms.topic: reference
tech.root: directml
ms.date: 11/04/2020
req.header: directml.h
req.include-header: ''
req.target-type: Windows
req.target-min-winverclnt: ''
req.target-min-winversvr: ''
req.kmdf-ver: ''
req.umdf-ver: ''
req.ddi-compliance: ''
req.unicode-ansi: ''
req.idl: ''
req.max-support: ''
req.namespace: ''
req.assembly: ''
req.type-library: ''
req.lib: DirectML.lib
req.dll: DirectML.dll
req.irql: ''
targetos: Windows
req.typenames: ''
req.redist: ''
f1_keywords:
- IDMLDevice1::CompileGraph
- directml/IDMLDevice1::CompileGraph
dev_langs:
- c++
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- DirectML.dll
api_name:
- IDMLDevice1.CompileGraph
ms.openlocfilehash: 25dbc62fac9cd38d9728a295e336038441aee19f
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/10/2021
ms.locfileid: "105721214"
---
# <a name="idmldevice1compilegraph-method-directmlh"></a>IDMLDevice1:: CompileGraph (método) (directml. h)

Compila un grafo de operadores de DirectML en un objeto que se puede enviar a la GPU.

Un operador compilado representa la forma eficaz y horneada de un operador adecuado para su ejecución en la GPU. Un operador compilado mantiene el estado (como los sombreadores y otros objetos) necesarios para la ejecución. Dado que un operador compilado implementa la interfaz [IDMLPageable](/windows/win32/api/directml/nn-directml-idmlpageable) , puede expulsar una de la memoria de GPU si lo desea. Vea [IDMLDevice1:: expulsión](/windows/win32/api/directml/nf-directml-idmldevice-evict) y [IDMLDevice1:: MakeResident](/windows/win32/api/directml/nf-directml-idmldevice-makeresident) para obtener más información.

El operador compilado no usa ni hace referencia a los objetos [IDMLOperator](/windows/win32/api/directml/nn-directml-idmloperator) proporcionados en la descripción del gráfico después de que este método devuelva.

> [!IMPORTANT]
> Esta API está disponible como parte del paquete redistribuible de DirectML independiente (consulte [Microsoft. AI. DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/). Consulte también el [historial de versiones de DirectML](../dml-version-history.md).

## <a name="syntax"></a>Sintaxis

```cpp
HRESULT CompileGraph(
  const DML_GRAPH_DESC *desc,
  DML_EXECUTION_FLAGS  flags,
  REFIID               riid,
  void                 **ppv
);
```

## <a name="parameters"></a>Parámetros

`desc`

Tipo: **[DML_GRAPH_DESC](./ns-directml-dml_graph_desc.md)\***

Descripción del gráfico que se va a compilar. Vea [DML_GRAPH_DESC](./ns-directml-dml_graph_desc.md).

`flags`

Tipo: [ **DML_EXECUTION_FLAGS**](/windows/win32/api/directml/ne-directml-dml_execution_flags)

Cualquier marcador para controlar la ejecución de este operador.

`riid`

Tipo: <b>REFIID</b>

Referencia al identificador único global (GUID) de la interfaz que desea que se devuelva en <i>PPV</i>. Se espera que sea el GUID de [IDMLCompiledOperator](/windows/win32/api/directml/nn-directml-idmlcompiledoperator).

`ppv`

Tipo: <b>void * *</b>

Un puntero a un bloque de memoria que recibe un puntero al operador compilado. Se trata de la dirección de un puntero a un [IDMLCompiledOperator](/windows/win32/api/directml/nn-directml-idmlcompiledoperator), que representa el operador compilado creado.


## <a name="return-value"></a>Valor devuelto

Tipo: [ **HRESULT**](/windows/desktop/winprog/windows-data-types)

Si este método se ejecuta correctamente, devuelve **S_OK**. De lo contrario, devuelve un código de error **HRESULT** .

## <a name="remarks"></a>Observaciones

La API del operador DirectML proporciona una manera abstracta de usar DirectML de forma eficaz en diverso hardware. DirectML aplica optimizaciones de nivel de tensores, como elegir el diseño de tensores más eficaz basado en el adaptador que se está usando. También aplica optimizaciones como la eliminación de operadores de combinación o de división.

Se recomienda aplicar optimizaciones de alto nivel antes de compilar un gráfico de DirectML. Por ejemplo, fusionar operadores de convolución con BatchNorm, plegamiento de constantes y eliminación común de subexpresiones. Las optimizaciones del optimizador de gráficos de DirectML están diseñadas para complementar estas optimizaciones independientes del dispositivo, que normalmente se administran de forma genérica mediante marcos de aprendizaje automático.

## <a name="requirements"></a>Requisitos
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Plataforma de destino** | Windows |
| **Header** | directml. h |
| **Library** | DirectML. lib |
| **DLL** | DirectML.dll |

## <a name="see-also"></a>Vea también

[IDMLDevice1](/windows/win32/api/directml/nn-directml-idmldevice)