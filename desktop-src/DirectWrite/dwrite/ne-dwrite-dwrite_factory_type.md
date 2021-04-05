---
UID: NE:dwrite.DWRITE_FACTORY_TYPE
title: DWRITE_FACTORY_TYPE (dwrite.h)
description: Especifica el tipo de objeto de generador de DirectWrite.
tech.root: DirectWrite
ms.date: 11/11/2020
ms.topic: reference
req.header: dwrite.h
req.include-header: dwrite_core.h
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
- DWRITE_FACTORY_TYPE
- dwrite/DWRITE_FACTORY_TYPE
dev_langs:
- c++
topic_type:
- APIRef
- kbSyntax
api_type:
- HeaderDef
api_location:
- dwrite.h
api_name:
- DWRITE_FACTORY_TYPE
ms.openlocfilehash: 603b2ae525ddc6472a3b8581627f2877e06d1aac
ms.sourcegitcommit: dd4a3716477b1363be58ecc0d439029f81467104
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/11/2020
ms.locfileid: "104078792"
---
# <a name="dwrite_factory_type-enumeration-dwriteh"></a>Enumeración DWRITE_FACTORY_TYPE (DWRITE. h)

Especifica el tipo de objeto de generador de DirectWrite.

> [!IMPORTANT]
> Esta API está disponible como parte de la implementación de DWriteCore de [DirectWrite](../direct-write-portal.md). DWriteCore es una forma de DirectWrite que se ejecuta en versiones de Windows hasta Windows 8, y que le permite su uso en varias plataformas. Para obtener más información y ejemplos de código, consulte [información general de DWriteCore](/windows/win32/DirectWrite/dwrite/dwritecore-overview).

## <a name="syntax"></a>Sintaxis
```cpp
typedef enum DWRITE_FACTORY_TYPE {
  DWRITE_FACTORY_TYPE_SHARED,
  DWRITE_FACTORY_TYPE_ISOLATED,
  DWRITE_FACTORY_TYPE_RESTRICTED
} ;
```

## <a name="constants"></a>Constantes

| Nombre | Descripción |
| ---- |:---- |
| DWRITE_FACTORY_TYPE_SHARED | Indica que el generador de DirectWrite es un generador compartido y que permite la reutilización de datos de fuentes almacenados en memoria caché en varios componentes en proceso. Estos generadores también aprovechan los componentes de almacenamiento en caché de fuentes entre procesos para mejorar el rendimiento. |
| DWRITE_FACTORY_TYPE_ISOLATED | Indica que el objeto de generador de DirectWrite está aislado. Los objetos creados a partir del generador aislado no interactúan con el estado interno de DirectWrite desde otros componentes. |
| DWRITE_FACTORY_TYPE_RESTRICTED | Los objetos creados a partir de un generador restringido no usan ni modifican los datos de estado interno o almacenados en caché usados por otros generadores. Además, la colección de fuentes del sistema solo contiene fuentes conocidas.|

## <a name="examples"></a>Ejemplos

Consulte el tema de [información general de DWriteCore](/windows/win32/DirectWrite/dwrite/dwritecore-overview) y la aplicación de ejemplo [DWriteCoreGallery](https://github.com/microsoft/Project-Reunion-Samples/tree/main/DWriteCore/DWriteCoreGallery) .

## <a name="remarks"></a>Observaciones

Un objeto de generador de DirectWrite contiene información sobre su estado interno, como el registro del cargador de fuentes y los datos de fuentes en caché. En la mayoría de los casos, debe usar el objeto de generador compartido, ya que permite que varios componentes que usan DirectWrite compartan información interna de estado de DirectWrite, lo que reduce el uso de memoria. Sin embargo, hay casos en los que es deseable reducir el impacto de un componente en el resto del proceso, como un complemento de un origen que no es de confianza, mediante el espacio aislado y el aislamiento del resto de los componentes del proceso. En tales casos, debe usar un generador aislado para el componente de espacio aislado.

Un generador restringido está más bloqueado que un generador aislado. No interactúa de ningún modo con una memoria caché de fuentes entre procesos ni persistentes. Además, la colección de fuentes del sistema devuelta desde este generador solo incluye fuentes conocidas. Si pasa **DWRITE_FACTORY_TYPE_RESTRICTED** a una versión de DWRITE anterior a DWriteCore, [DWriteCreateFactory](/windows/win32/api/dwrite/nf-dwrite-dwritecreatefactory) devuelve **E_INVALIDARG**.

## <a name="requirements"></a>Requisitos
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Cliente mínimo compatible** | Windows 10, versión preliminar de Project reunion 0,1 [aplicaciones Win32] |
| **Header** | dwrite. h (incluir dwrite_core. h) |
