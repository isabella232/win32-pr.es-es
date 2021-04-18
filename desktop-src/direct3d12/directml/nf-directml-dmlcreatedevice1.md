---
UID: NF:directml.DMLCreateDevice1
title: Función DMLCreateDevice1
description: Crea un dispositivo DirectML para un dispositivo Direct3D 12 determinado.
helpviewer_keywords:
- DMLCreateDevice1
- DMLCreateDevice1 function
- direct3d12.dmlcreatedevice1
- directml/DMLCreateDevice1
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
- DMLCreateDevice1
- directml/DMLCreateDevice1
dev_langs:
- c++
topic_type:
- APIRef
- kbSyntax
api_type:
- DllExport
api_location:
- DirectML.dll
api_name:
- DMLCreateDevice1
ms.openlocfilehash: f40c7e6aa82644b67303bc60f6a8b41fa08c6f8d
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/10/2021
ms.locfileid: "105721241"
---
# <a name="dmlcreatedevice1-function-directmlh"></a>Función DMLCreateDevice1 (directml. h)

Crea un dispositivo DirectML para un dispositivo Direct3D 12 determinado.

> [!IMPORTANT]
> Esta API está disponible como parte del paquete redistribuible de DirectML independiente (consulte [Microsoft. AI. DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/). Consulte también el [historial de versiones de DirectML](../dml-version-history.md).

## <a name="syntax"></a>Sintaxis

```cpp
HRESULT DMLCreateDevice1(
  ID3D12Device            *d3d12Device,
  DML_CREATE_DEVICE_FLAGS flags,
  DML_FEATURE_LEVEL       minimumFeatureLevel,
  REFIID                  riid,
  void                    **ppv
);
```

## <a name="parameters"></a>Parámetros

`d3d12Device`

Tipo: <b> <a href="/windows/win32/api/d3d12/nn-d3d12-id3d12device">ID3D12Device</a>*</b>

Un puntero a un [ID3D12Device](/windows/win32/api/d3d12/nn-d3d12-id3d12device) que representa el dispositivo de Direct3D 12 en el que se va a crear el dispositivo DirectML. DirectML admite cualquier nivel de características D3D y dispositivos Direct3D 12 creados en cualquier adaptador, incluido WARP. Sin embargo, no todas las características de DirectML pueden estar disponibles en función de las capacidades del dispositivo Direct3D 12. Vea [IDMLDevice:: CheckFeatureSupport](/windows/win32/api/directml/nf-directml-idmldevice-checkfeaturesupport) para obtener más información.

Si la llamada a **DMLCreateDevice1** se realiza correctamente, el dispositivo DirectML mantiene una referencia segura al dispositivo Direct3D 12 proporcionado.

`flags`

Tipo: <b>DML_CREATE_DEVICE_FLAGS</b>

Un valor [DML_CREATE_DEVICE_FLAGS](/windows/win32/api/directml/ne-directml-dml_create_device_flags) que especifica las opciones de creación de dispositivos adicionales.

`minimumFeatureLevel`

Tipo: <b>DML_FEATURE_LEVEL</b>

Un valor [DML_FEATURE_LEVEL](/windows/win32/api/directml/ne-directml-dml_feature_level) que especifica la compatibilidad mínima de nivel de característica requerida.

Este parámetro puede ser útil para los llamadores que requieran una versión específica de DirectML, pero que pueden encontrarse llamando a una versión anterior de DirectML. Esto puede ocurrir, por ejemplo, cuando el usuario ejecuta la aplicación en una versión anterior de Windows 10.

Las aplicaciones que dependen explícitamente de la funcionalidad introducida en un nivel de característica determinado pueden especificarla como *minimumFeatureLevel*. Esto garantizará que **DMLCreateDevice1** no se realizará correctamente a menos que la implementación subyacente sea *al menos* tan eficaz como sea el nivel de característica mínimo solicitado.

Tenga en cuenta que como este parámetro especifica un nivel de característica *mínimo* , el dispositivo DirectML subyacente puede, de hecho, admitir un nivel de características superior al mínimo solicitado. Una vez que la creación del dispositivo se realiza correctamente, puede consultar todos los niveles de características admitidos por este dispositivo mediante [IDMLDevice:: CheckFeatureSupport](/windows/win32/api/directml/nf-directml-idmldevice-checkfeaturesupport).

`riid`

Tipo: <b>REFIID</b>

Referencia al identificador único global (GUID) de la interfaz que desea que se devuelva en el <i>dispositivo</i>. Se espera que sea el GUID de [IDMLDevice](/windows/win32/api/directml/nn-directml-idmldevice).

`ppv`

Tipo: \_ com \_ Outptr \_ OPC \_ <b>void * *</b>

Un puntero a un bloque de memoria que recibe un puntero al dispositivo. Se trata de la dirección de un puntero a un [IDMLDevice](/windows/win32/api/directml/nn-directml-idmldevice), que representa el dispositivo DirectML creado.


## <a name="return-value"></a>Valor devuelto

Tipo: [ **HRESULT**](/windows/desktop/winprog/windows-data-types)

Si la función se ejecuta correctamente, devuelve <b>S_OK</b>. De lo contrario, devuelve un código de error [HRESULT](/windows/desktop/winprog/windows-data-types) .

Si esta versión de DirectML no admite el *minimumFeatureLevel* solicitado, esta función devolverá **DXGI_ERROR_UNSUPPORTED**.

La característica de herramientas de gráficos a petición (du) debe estar instalada para poder usar las capas de depuración de DirectML. Si la marca de [DML_CREATE_DEVICE_FLAG_DEBUG](/windows/win32/api/directml/ne-directml-dml_create_device_flags) se especifica en *marcas* y las capas de depuración no están instaladas, **DMLCreateDevice1** devuelve **DXGI_ERROR_SDK_COMPONENT_MISSING**.

## <a name="remarks"></a>Observaciones

Se presentó una versión más reciente de esta función, [DMLCreateDevice1](), en DirectML versión 1.1.0. **DMLCreateDevice1** es equivalente a llamar a **DMLCreateDevice1** y proporcionar un *minimumFeatureLevel* de [DML_FEATURE_LEVEL_1_0](/windows/win32/api/directml/ne-directml-dml_feature_level).

## <a name="availability"></a>Disponibilidad

Esta API se presentó en la versión DirectML `1.1.0` .

## <a name="requirements"></a>Requisitos
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Plataforma de destino** | Windows |
| **Header** | directml. h |
| **Library** | DirectML. lib |
| **DLL** | DirectML.dll |

## <a name="see-also"></a>Vea también

* [Enumeración DML_FEATURE_LEVEL](/windows/win32/api/directml/ne-directml-dml_feature_level)
* [Historial de versiones de DirectML](../dml-version-history.md)
* [Historial de nivel de característica de DirectML](/windows/win32/direct3d12/dml-feature_level-history)    
* [Usar la capa de depuración DirectML](../dml-debug-layer.md)