---
title: IEnumSTATPROPSETSTG-Compound de archivos
description: La implementación de archivo compuesto de la interfaz IEnumSTATPROPSETSTG se usa para enumerar una matriz de estructuras STATPROPSETSTG que contienen datos de propiedades estadísticas.
ms.assetid: 1ce36e40-518c-411b-be5a-835a2dd0995e
keywords:
- IEnumSTATPROPSETSTG Strctd Stg , implementación de archivos compuestos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ed34688f4967263649c828ab76b73b4d5150142ffa826e291fa4a0cfb7f50750
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119663035"
---
# <a name="ienumstatpropsetstg-compound-file-implementation"></a>IEnumSTATPROPSETSTG-Compound de archivos

La implementación de archivo compuesto de [**la interfaz IEnumSTATPROPSETSTG**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropsetstg) se usa para enumerar una matriz de estructuras [**STATPROPSETSTG**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropsetstg) que contienen datos de propiedades estadísticas. La [**implementación de IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) administra los datos estadísticos y está asociada a un objeto de almacenamiento de archivos compuesto actual.

## <a name="when-to-use"></a>Cuándo usar

Llame a los métodos de [**IEnumSTATPROPSETSTG**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropsetstg) para enumerar las estructuras [**STATPROPSETSTG,**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropsetstg) cada una de las cuales proporciona datos sobre uno de los conjuntos de propiedades asociados al objeto de almacenamiento de archivos compuesto.

## <a name="remarks"></a>Comentarios

<dl> <dt>

<span id="IEnumSTATPROPSETSTG__Next"></span><span id="ienumstatpropsetstg__next"></span><span id="IENUMSTATPROPSETSTG__NEXT"></span>[**IEnumSTATPROPSETSTG::Next**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropstg)
</dt> <dd>

Obtiene la siguiente o varias estructuras [**STATPROPSETSTG**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropsetstg) (el número se especifica mediante el *parámetro celt).* Los **elementos STATPROPSETSTG proporcionados** a través de una llamada a la implementación de archivo compuesto [**de IEnumSTATPROPSETSTG::Next**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropstg) siguen estas reglas:

-   Si [**IEnumSTATPROPSETSTG::Next**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropstg) no puede proporcionar STATPROPSETSTG.fmtid, se escriben ceros en ese miembro. Esto sucede cuando el conjunto de propiedades no tiene un nombre predefinido (como \\ 005SummaryInformation) y no es un valor legal.
-   El conjunto de propiedades DocumentSummaryInformation y UserDefined es especial, ya que puede tener dos secciones de conjunto de propiedades. Este conjunto de propiedades se describe en la sección [The DocumentSummaryInformation and UserDefined Property Sets](the-documentsummaryinformation-and-userdefined-property-sets.md). La segunda sección se conoce como propiedades User-Defined propiedades. Cada sección se identifica con un identificador de formato único (FMTID). Cuando [**se usa IPropertySetStorage::Enum**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-enum) para enumerar conjuntos de propiedades, User-Defined conjunto de propiedades no se enumerará.

> [!Note]  
> Si siempre crea un conjunto de propiedades mediante [**IPropertySetStorage::Create**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-create), como se crea un "GUID de caracteres" para el nombre de almacenamiento, [**IEnumSTATPROPSETSTG::Next**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropstg) devolverá un FMTID válido distinto de cero para el conjunto de propiedades \[ STATPROPSETSTG.fmtid. \]

 

-   El miembro STATPROPSETSTG.grfFlags no refleja necesariamente si el conjunto de propiedades es ANSI o no. Si se establece PROPSETFLAG \_ ANSI, el conjunto de propiedades es definitivamente ANSI. Si PROPSETFLAG ANSI está claro, el conjunto de propiedades podría ser Unicode o no Unicode, porque no es posible saber si es ANSI sin \_ abrirlo.
-   El miembro STATPROPSETSTG.grfFlags refleja si el conjunto de propiedades es simple o no, por lo que la configuración de la marca PROPSETFLAG NONSIMPLE siempre \_ es válida.
-   Si [**IEnumSTATPROPSETSTG::Next**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropstg) no puede proporcionar STATPROPSETSTG.clsid, se establece en todos los ceros (CLSID \_ NULL). En la implementación del archivo compuesto COM, esto ocurre cuando el conjunto de propiedades es simple (no se ha establecido la marca PROPSETFLAG NONSIMPLE) o no es sencillo, pero el CLSID no se estableció \_ explícitamente. En el caso de los conjuntos de propiedades no simples, el CLSID que se recibe es el que mantiene el [**elemento IStorage subyacente.**](/windows/desktop/api/Objidl/nn-objidl-istorage)
-   Si [**IEnumSTATPROPSETSTG::Next**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropstg) no puede proporcionar los campos de tiempo \[ **ctime**, **mtime**, **atime**, cada hora no admitida se establecerá \] en ceros. En la implementación del archivo compuesto COM, la obtención de estos valores depende de recuperarlos de la implementación [**subyacente de IStorage.**](/windows/desktop/api/Objidl/nn-objidl-istorage)

</dd> <dt>

<span id="IEnumSTATPROPSETSTG__Skip"></span><span id="ienumstatpropsetstg__skip"></span><span id="IENUMSTATPROPSETSTG__SKIP"></span>[**IEnumSTATPROPSETSTG::Skip**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropsetstg)
</dt> <dd>

Omite el número de elementos especificados en *celt*. Devuelve S OK si se omite el número especificado de elementos y devuelve S FALSE si se omiten menos elementos de los \_ \_ solicitados. En cualquier otro caso, devuelve el error adecuado.

</dd> <dt>

<span id="IEnumSTATPROPSETSTG__Reset"></span><span id="ienumstatpropsetstg__reset"></span><span id="IENUMSTATPROPSETSTG__RESET"></span>[**IEnumSTATPROPSETSTG::Reset**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropsetstg)
</dt> <dd>

Establece el cursor al principio de la enumeración . Si se realiza correctamente, devuelve S \_ OK; de lo contrario, devuelve STG \_ E \_ INVALIDHANDLE.

</dd> <dt>

<span id="IEnumSTATPROPSETSTG__Clone"></span><span id="ienumstatpropsetstg__clone"></span><span id="IENUMSTATPROPSETSTG__CLONE"></span>[**IEnumSTATPROPSETSTG::Clone**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropsetstg)
</dt> <dd>

Copia el estado de enumeración actual de este enumerador.

</dd> </dl>

 

 