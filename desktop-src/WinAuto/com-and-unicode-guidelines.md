---
title: Instrucciones COM y Unicode
description: Dado Microsoft Active Accessibility se basa en el modelo de objetos componentes (COM), los desarrolladores necesitan un nivel moderado de comprensión sobre los objetos COM e interfaces y deben saber cómo realizar tareas básicas (por ejemplo, cómo inicializar la biblioteca COM).
ms.assetid: ed4bbef9-676a-4f4e-926a-044f71399c56
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a2312b6177891c31c0987b846f7adfc1aa08abc7
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127570057"
---
# <a name="com-and-unicode-guidelines"></a>Instrucciones COM y Unicode

Dado Microsoft Active Accessibility se basa en el modelo de objetos componentes (COM), los desarrolladores necesitan un nivel moderado de comprensión sobre los objetos COM e interfaces y deben saber cómo realizar tareas básicas (por ejemplo, cómo inicializar la biblioteca COM). Los desarrolladores de servidores deben comprender cómo diseñar clases que implementan la [**interfaz IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) y cómo crear objetos accesibles.

También necesita un nivel moderado de comprensión sobre Unicode para usar muchas de las Microsoft Active Accessibility que devuelven cadenas.

Para usar Microsoft Active Accessibility de forma eficaz, debe comprender las siguientes funciones, estructuras, tipos de datos e interfaces COM y Unicode. En esta documentación se proporciona información limitada sobre algunos de estos elementos.

### <a name="functions"></a>Funciones:

-   [**OleInitialize**](/windows/desktop/api/ole2/nf-ole2-oleinitialize)
-   [**CoInitialize**](/windows/desktop/api/objbase/nf-objbase-coinitialize) o [ **CoInitializeEx**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializeex)
-   [**IUnknown::AddRef**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-addref) e [ **IUnknown::Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release)
-   [**VariantInit**](/previous-versions/windows/desktop/api/oleauto/nf-oleauto-variantinit) y [ **VariantClear**](/previous-versions/windows/desktop/api/oleauto/nf-oleauto-variantclear)
-   [**MultiByteToWideChar**](/windows/desktop/api/stringapiset/nf-stringapiset-multibytetowidechar) y [ **WideCharToMultiByte**](/windows/desktop/api/stringapiset/nf-stringapiset-widechartomultibyte)
-   [**SysAllocString**](/previous-versions/windows/desktop/api/oleauto/nf-oleauto-sysallocstring) y [ **SysFreeString**](/previous-versions/windows/desktop/api/oleauto/nf-oleauto-sysfreestring)

### <a name="structures-and-data-types"></a>Estructuras y tipos de datos:

-   [**VARIANTE**](variant-structure.md)
-   [**HRESULT**](/windows/desktop/com/structure-of-com-error-codes)
-   [**BSTR**](/previous-versions/windows/desktop/automat/bstr)

### <a name="com-interfaces"></a>Interfaces COM:

-   [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown)
-   [**IDispatch**](idispatch-interface.md)
-   [**IEnumVARIANT**](/previous-versions/windows/desktop/api/oaidl/nn-oaidl-ienumvariant)

## <a name="in-this-section"></a>En esta sección

-   [VARIANT (estructura)](variant-structure.md)
-   [IDispatch (interfaz)](idispatch-interface.md)
-   [Convertir cadenas Unicode y ANSI](converting-unicode-and-ansi-strings.md)

 

 