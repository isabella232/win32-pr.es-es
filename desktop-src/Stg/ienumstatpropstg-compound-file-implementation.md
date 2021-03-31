---
title: IEnumSTATPROPSTG-Compound la implementación de archivos
description: La implementación de archivo compuesto de la interfaz IEnumSTATPROPSTG se usa para enumerar las propiedades, lo que da lugar a estructuras STATPROPSTG, que contienen datos de propiedad estadísticos.
ms.assetid: 8fa536f4-cce6-47e4-a860-2f43e48fa469
keywords:
- IEnumSTATPROPSTG Strctd STG, implementación de archivo compuesto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3bbffce14016efdb4e2a77d60096b6776e6c2189
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "103995529"
---
# <a name="ienumstatpropstg-compound-file-implementation"></a>IEnumSTATPROPSTG-Compound la implementación de archivos

La implementación de archivo compuesto de la interfaz [**IEnumSTATPROPSTG**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropstg) se usa para enumerar las propiedades, lo que da lugar a estructuras [**STATPROPSTG**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropstg) , que contienen datos de propiedad estadísticos. La implementación de [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) administra los datos estadísticos y está asociado a un objeto de almacenamiento de archivos compuesto actual.

El constructor de la implementación COM de [**IEnumSTATPROPSTG**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropstg) crea una clase que lee el conjunto de propiedades completo y crea una matriz estática que se puede compartir cuando se llama a **IEnumSTATPROPSTG:: Clone** .

## <a name="when-to-use"></a>Cuándo usar

Llame a la implementación de archivo compuesto de [**IEnumSTATPROPSTG**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropstg) para enumerar las estructuras [**STATPROPSTG**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropstg) que contienen datos sobre las propiedades del conjunto de propiedades actual. Al usar la implementación de archivo compuesto de las interfaces de almacenamiento de propiedades, llame a [**IPropertyStorage:: enum**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-enum) para devolver un puntero a **IEnumSTATPROPSTG** para administrar el objeto de almacenamiento de propiedades y los elementos que contiene.

## <a name="remarks"></a>Observaciones

<dl> <dt>

<span id="IEnumSTATPROPSTG__Next"></span><span id="ienumstatpropstg__next"></span><span id="IENUMSTATPROPSTG__NEXT"></span>[**IEnumSTATPROPSTG:: Next**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropstg)
</dt> <dd>

Obtiene la siguiente estructura [**STATPROPSTG**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropstg) o más (el número se especifica mediante el parámetro *Celt* ). Devuelve S \_ correcto si se realiza correctamente.

</dd> <dt>

<span id="IEnumSTATPROPSTG__Skip"></span><span id="ienumstatpropstg__skip"></span><span id="IENUMSTATPROPSTG__SKIP"></span>[**IEnumSTATPROPSTG:: Skip**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropstg)
</dt> <dd>

Omite el número de elementos especificados en *Celt*. El siguiente elemento que se va a enumerar a través de una llamada a Next se convierte en el elemento situado después de los elementos omitidos. Devuelve S \_ OK si se omitieron los elementos *Celt* ; devuelve s \_ false si se omitieron menos de *Celt* elementos.

</dd> <dt>

<span id="IEnumSTATPROPSTG__Reset"></span><span id="ienumstatpropstg__reset"></span><span id="IENUMSTATPROPSTG__RESET"></span>[**IEnumSTATPROPSTG:: RESET**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropstg)
</dt> <dd>

Establece el cursor al principio de la enumeración. Si se realiza correctamente, devuelve S \_ OK; de lo contrario, devuelve STG \_ E \_ INVALIDHANDLE.

</dd> <dt>

<span id="IEnumSTATPROPSTG__Clone"></span><span id="ienumstatpropstg__clone"></span><span id="IENUMSTATPROPSTG__CLONE"></span>[**IEnumSTATPROPSTG:: Clone**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropstg)
</dt> <dd>

Utiliza el constructor de [**IEnumSTATPROPSTG**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropstg) para crear una copia de la matriz. Dado que la clase que construye la matriz estática contiene realmente el objeto, esta función agrega principalmente al recuento de referencias.

</dd> </dl>

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**STATPROPSTG**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropstg)
</dt> <dt>

[**IPropertyStorage:: enum**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-enum)
</dt> </dl>

 

 