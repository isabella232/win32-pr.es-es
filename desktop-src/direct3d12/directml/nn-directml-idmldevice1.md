---
UID: NN:directml.IDMLDevice1
title: IDMLDevice1
description: Representa un dispositivo DirectML, que se usa para crear operadores, enlazar tablas, grabadores de comandos y otros objetos.
helpviewer_keywords:
- IDMLDevice1
- IDMLDevice1 interface
- IDMLDevice1 interface
- described
- direct3d12.idmldevice1
- directml/IDMLDevice1
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
req.lib: ''
req.dll: ''
req.irql: ''
targetos: Windows
req.typenames: ''
req.redist: ''
f1_keywords:
- IDMLDevice1
- directml/IDMLDevice1
dev_langs:
- c++
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- DirectML.h
api_name:
- IDMLDevice1
ms.openlocfilehash: a23d6ec4299a2aa3ca7e9f6873167412d094af8d
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/10/2021
ms.locfileid: "105721240"
---
# <a name="idmldevice1-interface-directmlh"></a>Interfaz IDMLDevice1 (directml. h)

Representa un dispositivo DirectML, que se usa para crear operadores, enlazar tablas, grabadores de comandos y otros objetos. La interfaz **IDMLDevice1** hereda de [IDMLDevice](/windows/win32/api/directml/nn-directml-idmldevice).

Un dispositivo DirectML siempre está asociado con exactamente un dispositivo Direct3D 12 subyacente. Todos los objetos creados por el dispositivo DirectML mantienen una referencia segura a su dispositivo primario. A diferencia del dispositivo Direct3D 12, el dispositivo DML no es un singleton. Por lo tanto, es posible crear varios dispositivos DirectML en el mismo dispositivo de Direct3D 12. Sin embargo, esto no se recomienda porque el dispositivo DirectML no tiene ningún estado mutable, por lo que hay poca ventaja en la creación de varios dispositivos DML en el mismo dispositivo de Direct3D 12.

Este objeto es seguro para subprocesos.

> [!IMPORTANT]
> Esta API está disponible como parte del paquete redistribuible de DirectML independiente (consulte [Microsoft. AI. DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/). Consulte también el [historial de versiones de DirectML](../dml-version-history.md).

## <a name="availability"></a>Disponibilidad
Esta API se presentó en la versión DirectML `1.1.0` .

## <a name="tensor-constraints"></a>Restricciones de tensores
**Plataforma de destino**: Windows


## <a name="inheritance"></a>Herencia


La interfaz IDMLDevice1 hereda de la interfaz IDMLDevice.



## <a name="methods"></a>Métodos

<p>La interfaz <b>IDMLDevice1</b> tiene estos métodos.</p>

| Método | Descripción |
| ---- |:---- |
| [IDMLDevice1::CompileGraph](../directml/nf-directml-idmldevice1-compilegraph.md) | Compila un grafo de operadores de DirectML en un objeto que se puede enviar a la GPU. |


## <a name="requirements"></a>Requisitos
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Plataforma de destino** | Windows |
| **Header** | directml. h |

## <a name="see-also"></a>Vea también

[Interfaz IDMLDevice](/windows/win32/api/directml/nn-directml-idmldevice)