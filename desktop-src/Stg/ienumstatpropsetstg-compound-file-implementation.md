---
title: IEnumSTATPROPSETSTG-Compound la implementación de archivos
description: La implementación de archivo compuesto de la interfaz IEnumSTATPROPSETSTG se usa para enumerar una matriz de estructuras STATPROPSETSTG que contienen datos de propiedad estadísticos.
ms.assetid: 1ce36e40-518c-411b-be5a-835a2dd0995e
keywords:
- IEnumSTATPROPSETSTG Strctd STG, implementación de archivo compuesto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9566af1a1956b3a951a996b6198f4a3161680042
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104359040"
---
# <a name="ienumstatpropsetstg-compound-file-implementation"></a>IEnumSTATPROPSETSTG-Compound la implementación de archivos

La implementación de archivo compuesto de la interfaz [**IEnumSTATPROPSETSTG**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropsetstg) se usa para enumerar una matriz de estructuras [**STATPROPSETSTG**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropsetstg) que contienen datos de propiedad estadísticos. La implementación de [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) administra los datos estadísticos y está asociado a un objeto de almacenamiento de archivos compuesto actual.

## <a name="when-to-use"></a>Cuándo usar

Llame a los métodos de [**IEnumSTATPROPSETSTG**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropsetstg) para enumerar las estructuras [**STATPROPSETSTG**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropsetstg) , cada una de las cuales proporciona datos sobre uno de los conjuntos de propiedades asociados al objeto de almacenamiento de archivos compuesto.

## <a name="remarks"></a>Observaciones

<dl> <dt>

<span id="IEnumSTATPROPSETSTG__Next"></span><span id="ienumstatpropsetstg__next"></span><span id="IENUMSTATPROPSETSTG__NEXT"></span>[**IEnumSTATPROPSETSTG:: Next**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropstg)
</dt> <dd>

Obtiene la siguiente estructura [**STATPROPSETSTG**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropsetstg) o más (el número se especifica mediante el parámetro *Celt* ). Los elementos **STATPROPSETSTG** que se proporcionan a través de una llamada a la implementación de archivo compuesto de [**IEnumSTATPROPSETSTG:: Next**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropstg) siguen estas reglas:

-   Si [**IEnumSTATPROPSETSTG:: Next**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropstg) no proporciona STATPROPSETSTG. fmtid, se escriben ceros en ese miembro. Esto sucede si el conjunto de propiedades no tiene un nombre predefinido (por ejemplo, \\ 005SummaryInformation) y no es un valor válido.
-   El conjunto de propiedades DocumentSummaryInformation y UserDefined es especial, ya que puede tener dos secciones set de propiedad. Este conjunto de propiedades se describe en la sección de [los conjuntos de propiedades DocumentSummaryInformation y UserDefined](the-documentsummaryinformation-and-userdefined-property-sets.md). La segunda sección se conoce como User-Defined propiedades. Cada sección se identifica con un identificador de formato único (FMTID). Cuando se usa [**IPropertySetStorage:: enum**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-enum) para enumerar los conjuntos de propiedades, no se enumerará el conjunto de propiedades User-Defined.

> [!Note]  
> Si siempre crea un conjunto de propiedades mediante [**IPropertySetStorage:: Create**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-create), porque se crea un "GUID de carácter" para el nombre de almacenamiento, [**IEnumSTATPROPSETSTG:: Next**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropstg) devolverá un FMTID válido distinto de cero para el conjunto de propiedades \[ STATPROPSETSTG. FMTID \] .

 

-   El miembro STATPROPSETSTG. grfFlags no refleja necesariamente si el conjunto de propiedades es ANSI o no. Si \_ se establece PROPSETFLAG ANSI, el conjunto de propiedades es definitivamente ANSI. Si PROPSETFLAG \_ ANSI está claro, el conjunto de propiedades podría ser Unicode o no Unicode, ya que no es posible saber si es ANSI sin abrirlo.
-   El miembro STATPROPSETSTG. grfFlags refleja si el conjunto de propiedades es simple o no, por lo que el valor de la \_ marca PROPSETFLAG nonsimple siempre es válido.
-   Si [**IEnumSTATPROPSETSTG:: Next**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropstg) no proporciona STATPROPSETSTG. CLSID, se establece en todos los ceros (CLSID \_ null). En la implementación de archivo compuesto COM, esto ocurre cuando el conjunto de propiedades es simple ( \_ no se establece la marca PROPSETFLAG no simple) o no es simple, pero el CLSID no se estableció explícitamente. En el caso de conjuntos de propiedades no simples, el CLSID que se recibe es el que mantiene el [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage)subyacente.
-   Si [**IEnumSTATPROPSETSTG:: Next**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropstg) no proporciona los campos de hora \[ **ctime**, **mtime**, **atime** \] , cada hora no admitida se establecerá en ceros. En la implementación de archivo compuesto COM, obtener estos valores depende de recuperarlos de la implementación de [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) subyacente.

</dd> <dt>

<span id="IEnumSTATPROPSETSTG__Skip"></span><span id="ienumstatpropsetstg__skip"></span><span id="IENUMSTATPROPSETSTG__SKIP"></span>[**IEnumSTATPROPSETSTG:: Skip**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropsetstg)
</dt> <dd>

Omite el número de elementos especificados en *Celt*. Devuelve S \_ OK si se omite el número especificado de elementos, devuelve s \_ false si se omiten menos elementos de los solicitados. En cualquier otro caso, devuelve el error adecuado.

</dd> <dt>

<span id="IEnumSTATPROPSETSTG__Reset"></span><span id="ienumstatpropsetstg__reset"></span><span id="IENUMSTATPROPSETSTG__RESET"></span>[**IEnumSTATPROPSETSTG:: RESET**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropsetstg)
</dt> <dd>

Establece el cursor al principio de la enumeración. Si se realiza correctamente, devuelve S \_ OK; de lo contrario, devuelve STG \_ E \_ INVALIDHANDLE.

</dd> <dt>

<span id="IEnumSTATPROPSETSTG__Clone"></span><span id="ienumstatpropsetstg__clone"></span><span id="IENUMSTATPROPSETSTG__CLONE"></span>[**IEnumSTATPROPSETSTG:: Clone**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropsetstg)
</dt> <dd>

Copia el estado actual de la enumeración de este enumerador.

</dd> </dl>

 

 