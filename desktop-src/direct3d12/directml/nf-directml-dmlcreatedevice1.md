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
ms.openlocfilehash: f722b12208bd808f01e177feb907f94c33541496
ms.sourcegitcommit: da68ed5718ec0e3aa0c252fc86ac3e275da91b82
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/04/2021
ms.locfileid: "111417943"
---
# <a name="dmlcreatedevice1-function-directmlh"></a>Función DMLCreateDevice1 (directml.h)

Crea un dispositivo DirectML para un dispositivo Direct3D 12 determinado.

> [!IMPORTANT]
> Esta API está disponible como parte del paquete redistribuible independiente de DirectML (consulte [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) versión 1.4 y posteriores). Consulte también Historial [de versiones de DirectML.](../dml-version-history.md)

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

Puntero a un [id3D12Dispositivo](/windows/win32/api/d3d12/nn-d3d12-id3d12device) que representa el dispositivo Direct3D 12 sobre el que se crea el dispositivo DirectML. DirectML admite cualquier nivel de característica D3D y dispositivos Direct3D 12 creados en cualquier adaptador, incluido WARP. Sin embargo, no todas las características de DirectML pueden estar disponibles en función de las funcionalidades del dispositivo Direct3D 12. Consulte [IDMLDevice::CheckFeatureSupport para](/windows/win32/api/directml/nf-directml-idmldevice-checkfeaturesupport) obtener más información.

Si la llamada a **DMLCreateDevice1** es correcta, el dispositivo DirectML mantiene una referencia fuerte al dispositivo Direct3D 12 proporcionado.

`flags`

Tipo: <b>DML_CREATE_DEVICE_FLAGS</b>

Valor [DML_CREATE_DEVICE_FLAGS](/windows/win32/api/directml/ne-directml-dml_create_device_flags) que especifica opciones de creación de dispositivos adicionales.

`minimumFeatureLevel`

Tipo: <b>DML_FEATURE_LEVEL</b>

Valor [DML_FEATURE_LEVEL](/windows/win32/api/directml/ne-directml-dml_feature_level) especifica la compatibilidad mínima de nivel de característica necesaria.

Este parámetro puede ser útil para los llamadores que requieren una versión específica de DirectML, pero que pueden encontrarse llamando a una versión anterior de DirectML. Esto puede ocurrir, por ejemplo, cuando el usuario ejecuta la aplicación en una versión anterior de Windows 10.

Las aplicaciones que dependen explícitamente de la funcionalidad introducida en un nivel de característica determinado pueden especificarla como *minimumFeatureLevel*. Esto garantizará que **DMLCreateDevice1** no se realizará  correctamente a menos que la implementación subyacente sea al menos tan capaz como este nivel mínimo de características solicitado.

Tenga en cuenta que,  como este parámetro especifica un nivel mínimo de características, el dispositivo DirectML subyacente puede admitir de hecho un nivel de característica superior al mínimo solicitado. Una vez que la creación del dispositivo se realiza correctamente, puede consultar todos los niveles de características compatibles con este dispositivo mediante [IDMLDevice::CheckFeatureSupport](/windows/win32/api/directml/nf-directml-idmldevice-checkfeaturesupport).

`riid`

Tipo: <b>REFIID</b>

Referencia al identificador único global (GUID) de la interfaz que desea que se devuelva en el <i>dispositivo</i>. Se espera que sea el GUID de [IDMLDevice.](/windows/win32/api/directml/nn-directml-idmldevice)

`ppv`

Tipo: \_ COM \_ Outptr opt \_ \_ <b>void**</b>

Puntero a un bloque de memoria que recibe un puntero al dispositivo. Esta es la dirección de un puntero a [un IDMLDevice](/windows/win32/api/directml/nn-directml-idmldevice), que representa el dispositivo DirectML creado.


## <a name="return-value"></a>Valor devuelto

Tipo: [ **HRESULT**](/windows/desktop/winprog/windows-data-types)

Si la función se realiza correctamente, devuelve <b>S_OK</b>. De lo contrario, devuelve un código de error [HRESULT.](/windows/desktop/winprog/windows-data-types)

Si esta versión de DirectML no admite la *solicitud minimumFeatureLevel,* esta función devolverá **DXGI_ERROR_UNSUPPORTED**.

La característica Herramientas de gráficos a petición (FOD) debe estar instalada para poder usar las capas de depuración de DirectML. Si la [DML_CREATE_DEVICE_FLAG_DEBUG](/windows/win32/api/directml/ne-directml-dml_create_device_flags) se especifica en *las* marcas y las capas de depuración no están instaladas, **DMLCreateDevice1** devuelve **DXGI_ERROR_SDK_COMPONENT_MISSING**.

## <a name="remarks"></a>Comentarios

Se introdujo una versión más reciente de esta función, [DMLCreateDevice1,]()en la versión 1.1.0 de DirectML. **DMLCreateDevice1 equivale** a llamar a **DMLCreateDevice1** y proporcionar un *minimumFeatureLevel* de [DML_FEATURE_LEVEL_1_0](/windows/win32/api/directml/ne-directml-dml_feature_level).

## <a name="availability"></a>Disponibilidad

Esta API se introdujo en la versión de `1.1.0` DirectML.

## <a name="requirements"></a>Requisitos
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Plataforma de destino** | Windows |
| **Header** | directml.h |
| **Library** | DirectML.lib |
| **Dll** | DirectML.dll |

## <a name="see-also"></a>Vea también

* [DML_FEATURE_LEVEL enumeración](/windows/win32/api/directml/ne-directml-dml_feature_level)
* [Historial de versiones de DirectML](../dml-version-history.md)
* [Historial de nivel de característica de DirectML](/windows/win32/direct3d12/dml-feature_level-history)    
* [Uso de la capa de depuración de DirectML](../dml-debug-layer.md)