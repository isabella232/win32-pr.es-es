---
UID: NF:directml.IDMLDevice1.CompileGraph
title: IDMLDevice1::CompileGraph
description: Compila un gráfico de operadores de DirectML en un objeto que se puede enviar a la GPU.
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
ms.openlocfilehash: 8a9b4ce9bd8f8bd8b1d6f2a6bbd144009eb0d79d
ms.sourcegitcommit: da68ed5718ec0e3aa0c252fc86ac3e275da91b82
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/04/2021
ms.locfileid: "111417940"
---
# <a name="idmldevice1compilegraph-method-directmlh"></a>Método IDMLDevice1::CompileGraph (directml.h)

Compila un gráfico de operadores de DirectML en un objeto que se puede enviar a la GPU.

Un operador compilado representa la forma eficaz y al día de un operador adecuado para su ejecución en la GPU. Un operador compilado contiene el estado (como sombreadores y otros objetos) necesario para la ejecución. Dado que un operador compilado implementa la interfaz [IDMLPageable,](/windows/win32/api/directml/nn-directml-idmlpageable) puede expulsar una de la memoria de GPU si lo desea. Vea [IDMLDevice1::Evict](/windows/win32/api/directml/nf-directml-idmldevice-evict) e [IDMLDevice1::MakeResident](/windows/win32/api/directml/nf-directml-idmldevice-makeresident) para obtener más información.

El operador compilado no usa ni hace referencia a los objetos [IDMLOperator](/windows/win32/api/directml/nn-directml-idmloperator) proporcionados en la descripción del gráfico después de que este método vuelva.

> [!IMPORTANT]
> Esta API está disponible como parte del paquete redistribuible independiente de DirectML (consulte [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) versión 1.4 y posteriores). Consulte también Historial [de versiones de DirectML.](../dml-version-history.md)

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

Descripción del gráfico que se compilará. Vea [DML_GRAPH_DESC](./ns-directml-dml_graph_desc.md).

`flags`

Tipo: [ **DML_EXECUTION_FLAGS**](/windows/win32/api/directml/ne-directml-dml_execution_flags)

Cualquier marca para controlar la ejecución de este operador.

`riid`

Tipo: <b>REFIID</b>

Referencia al identificador único global (GUID) de la interfaz que desea que se devuelva en <i>ppv.</i> Se espera que sea el GUID de [IDMLCompiledOperator.](/windows/win32/api/directml/nn-directml-idmlcompiledoperator)

`ppv`

Tipo: <b>void**</b>

Puntero a un bloque de memoria que recibe un puntero al operador compilado. Esta es la dirección de un puntero a [un IDMLCompiledOperator](/windows/win32/api/directml/nn-directml-idmlcompiledoperator), que representa el operador compilado creado.


## <a name="return-value"></a>Valor devuelto

Tipo: [ **HRESULT**](/windows/desktop/winprog/windows-data-types)

Si este método se realiza correctamente, devuelve **S_OK**. De lo contrario, devuelve un código de error **HRESULT.**

## <a name="remarks"></a>Comentarios

Graph API de operador de DirectML proporciona una manera abstracta de usar DirectML de forma eficaz en diversos hardware. DirectML aplica optimizaciones de nivel de tensor, como elegir el diseño de tensor más eficaz en función del adaptador que se usa. También aplica optimizaciones como la eliminación de operadores Join o Split.

Se recomienda aplicar optimizaciones de alto nivel antes de crear un gráfico de DirectML. Por ejemplo, la conversión de operadores de Convolution con BatchNorm, el plegado constante y la eliminación de subexpresión común. Las optimizaciones del optimizador de grafos de DirectML están diseñadas para complementar dichas optimizaciones independientes del dispositivo, que normalmente se controlan de forma genérica mediante marcos de aprendizaje automático.

## <a name="requirements"></a>Requisitos
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Plataforma de destino** | Windows |
| **Header** | directml.h |
| **Library** | DirectML.lib |
| **Dll** | DirectML.dll |

## <a name="see-also"></a>Vea también

[IDMLDevice1](/windows/win32/api/directml/nn-directml-idmldevice)