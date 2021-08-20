---
title: IEnumSTATPROPSTG-Compound de archivos
description: La implementación de archivo compuesto de la interfaz IEnumSTATPROPSTG se usa para enumerar las propiedades, lo que da lugar a estructuras STATPROPSTG, que contienen datos estadísticos de propiedades.
ms.assetid: 8fa536f4-cce6-47e4-a860-2f43e48fa469
keywords:
- IEnumSTATPROPSTG Strctd Stg , implementación de archivos compuestos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6a8c00cd8111e7669030af7d201c567397c951b31d4981784704da903821368b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117961824"
---
# <a name="ienumstatpropstg-compound-file-implementation"></a>IEnumSTATPROPSTG-Compound de archivos

La implementación de archivo compuesto de la [**interfaz IEnumSTATPROPSTG**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropstg) se usa para enumerar las propiedades, lo que da lugar a estructuras [**STATPROPSTG,**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropstg) que contienen datos estadísticos de propiedades. La implementación de [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) administra los datos estadísticos y está asociada a un objeto de almacenamiento de archivos compuesto actual.

El constructor de la implementación COM de [**IEnumSTATPROPSTG**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropstg) crea una clase que lee todo el conjunto de propiedades y crea una matriz estática que se puede compartir cuando se llama a **IEnumSTATPROPSTG::Clone.**

## <a name="when-to-use"></a>Cuándo usar

Llame a la implementación de archivo compuesto de [**IEnumSTATPROPSTG para**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropstg) enumerar las estructuras [**STATPROPSTG**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropstg) que contienen datos sobre las propiedades dentro del conjunto de propiedades actual. Al usar la implementación de archivo compuesto de las interfaces de almacenamiento de propiedades, llame a [**IPropertyStorage::Enum**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-enum) para devolver un puntero a **IEnumSTATPROPSTG** para administrar el objeto de almacenamiento de propiedades y los elementos que contiene.

## <a name="remarks"></a>Comentarios

<dl> <dt>

<span id="IEnumSTATPROPSTG__Next"></span><span id="ienumstatpropstg__next"></span><span id="IENUMSTATPROPSTG__NEXT"></span>[**IEnumSTATPROPSTG::Next**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropstg)
</dt> <dd>

Obtiene la siguiente o varias estructuras [**STATPROPSTG**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropstg) (el número se especifica mediante el *parámetro celt).* Devuelve S \_ OK si se realiza correctamente.

</dd> <dt>

<span id="IEnumSTATPROPSTG__Skip"></span><span id="ienumstatpropstg__skip"></span><span id="IENUMSTATPROPSTG__SKIP"></span>[**IEnumSTATPROPSTG::Skip**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropstg)
</dt> <dd>

Omite el número de elementos especificados en *celta.* El siguiente elemento que se va a enumerar mediante una llamada a Siguiente se convierte en el elemento después de los elementos omitido. Devuelve S \_ OK si se *omitieron los elementos celta;* devuelve S FALSE si se omitieron menos \_ de *celta.*

</dd> <dt>

<span id="IEnumSTATPROPSTG__Reset"></span><span id="ienumstatpropstg__reset"></span><span id="IENUMSTATPROPSTG__RESET"></span>[**IEnumSTATPROPSTG::Reset**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropstg)
</dt> <dd>

Establece el cursor al principio de la enumeración . Si se realiza correctamente, devuelve S \_ OK; de lo contrario, devuelve STG \_ E \_ INVALIDHANDLE.

</dd> <dt>

<span id="IEnumSTATPROPSTG__Clone"></span><span id="ienumstatpropstg__clone"></span><span id="IENUMSTATPROPSTG__CLONE"></span>[**IEnumSTATPROPSTG::Clone**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropstg)
</dt> <dd>

Usa el constructor para [**IEnumSTATPROPSTG**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropstg) para crear una copia de la matriz. Dado que la clase que construye la matriz estática contiene realmente el objeto , esta función agrega principalmente al recuento de referencias.

</dd> </dl>

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**STATPROPSTG**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropstg)
</dt> <dt>

[**IPropertyStorage::Enum**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-enum)
</dt> </dl>

 

 