---
UID: NE:dwrite.DWRITE_FACTORY_TYPE
title: DWRITE_FACTORY_TYPE (dwrite.h)
description: Especifica el tipo de objeto de generador DirectWrite.
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
ms.openlocfilehash: 87b0d1c2edcb836afd06d732f242b62441b9bd01
ms.sourcegitcommit: d7e9a20168111fb608f5fefb092b30f8e093d816
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/22/2021
ms.locfileid: "107881814"
---
# <a name="dwrite_factory_type-enumeration-dwriteh"></a>DWRITE_FACTORY_TYPE enumeración (dwrite.h)

Especifica el tipo de objeto de generador DirectWrite.

> [!IMPORTANT]
> Esta API está disponible como parte de la implementación de DWriteCore de [DirectWrite](../direct-write-portal.md). DWriteCore es una forma de DirectWrite que se ejecuta en versiones de Windows hasta Windows 8, y que le permite su uso en varias plataformas. Para obtener más información y ejemplos de código, vea Introducción a [DWriteCore.](/windows/win32/DirectWrite/dwrite/dwritecore-overview)

## <a name="syntax"></a>Sintaxis
```cpp
typedef enum DWRITE_FACTORY_TYPE {
  DWRITE_FACTORY_TYPE_SHARED,
  DWRITE_FACTORY_TYPE_ISOLATED,
  DWRITE_FACTORY_TYPE_ISOLATED2
} ;
```

## <a name="constants"></a>Constantes

| Nombre | Descripción |
| ---- |:---- |
| DWRITE_FACTORY_TYPE_SHARED | Indica que el generador de DirectWrite es un generador compartido y que permite reutilizar los datos de fuente almacenados en caché en varios componentes en proceso. Estos generadores también aprovechan los componentes de almacenamiento en caché de fuentes entre procesos para mejorar el rendimiento. |
| DWRITE_FACTORY_TYPE_ISOLATED | Indica que el objeto de generador DirectWrite está aislado. Los objetos creados a partir del generador aislado no interactúan con el estado interno de DirectWrite de otros componentes. |
| DWRITE_FACTORY_TYPE_ISOLATED2 | Indica que el objeto de generador DirectWrite está restringido. Los objetos creados a partir de una factoría restringida no usan ni modifican el estado interno ni los datos almacenados en caché que usan otros generadores. Además, la colección de fuentes del sistema solo contiene fuentes conocidas.|

## <a name="examples"></a>Ejemplos

Consulte el [tema de información general de DWriteCore](/windows/win32/DirectWrite/dwrite/dwritecore-overview) y la aplicación de ejemplo [DWriteCoreGallery.](https://github.com/microsoft/Project-Reunion-Samples/tree/main/DWriteCore/DWriteCoreGallery)

## <a name="remarks"></a>Observaciones

Un objeto de generador directWrite contiene información sobre su estado interno, como el registro del cargador de fuentes y los datos de fuente almacenados en caché. En la mayoría de los casos, debe usar el objeto de generador compartido, ya que permite que varios componentes que usan DirectWrite compartan información de estado interna de DirectWrite, lo que reduce el uso de memoria. Sin embargo, hay casos en los que es conveniente reducir el impacto de un componente en el resto del proceso, como un complemento de un origen que no es de confianza, mediante el espacio aislado y el aislamiento del resto de los componentes del proceso. En tales casos, debe usar un generador aislado para el componente de espacio aislado.

Una fábrica restringida está más bloqueada que una fábrica aislada. No interactúa con una caché de fuentes persistentes ni entre procesos de ninguna manera. Además, la colección de fuentes del sistema devuelta desde este generador incluye solo fuentes conocidas. Si pasa **DWRITE_FACTORY_TYPE_ISOLATED2** a una versión de DWrite anterior a [DWriteCore, DWriteCreateFactory](/windows/win32/api/dwrite/nf-dwrite-dwritecreatefactory) **devuelve E_INVALIDARG**.

## <a name="requirements"></a>Requisitos
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Cliente mínimo compatible** | Windows 10, Project Project Project [Aplicaciones Win32] |
| **Header** | dwrite.h (incluir dwrite_core.h) |
