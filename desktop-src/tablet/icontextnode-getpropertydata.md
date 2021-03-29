---
description: Recupera datos específicos de la aplicación u otros datos de propiedad para el identificador especificado.
ms.assetid: eaf95ff8-7b31-4c05-aa49-0c3bb9e996c0
title: 'IContextNode:: GetPropertyData (método) (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextNode.GetPropertyData
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 381d137dd73056a2a6f4c2e9cd3746f9f16c5b2e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103810034"
---
# <a name="icontextnodegetpropertydata-method"></a>IContextNode:: GetPropertyData (método)

Recupera datos específicos de la aplicación u otros datos de propiedad para el identificador especificado.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetPropertyData(
  [in]      const GUID  *pPropertyDataId,
  [in, out]       ULONG *pulPropertyDataSize,
  [out]           BYTE  **ppbPropertyData
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pPropertyDataId* \[ de\]
</dt> <dd>

El identificador de los datos.

</dd> <dt>

*pulPropertyDataSize* \[ in, out\]
</dt> <dd>

Tamaño de los datos en bytes. No se utiliza el valor que se pasa.

</dd> <dt>

*ppbPropertyData* \[ enuncia\]
</dt> <dd>

Puntero a una matriz de enteros de 8 bits sin signo que contiene los datos de la propiedad.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Para obtener una descripción de los valores devueltos, vea [clases e interfaces-análisis de tinta](classes-and-interfaces---ink-analysis.md).

## <a name="remarks"></a>Observaciones

> [!Caution]  
> Para evitar una pérdida de memoria, use [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree) para liberar la memoria de \* *ppbPropertyData* cuando ya no necesite la información.

 

Además de recuperar los datos específicos de la aplicación que se agregaron con [**IContextNode:: AddPropertyData**](icontextnode-addpropertydata.md), este método se usa para recuperar propiedades comunes que se describen en las constantes de [las propiedades del nodo de contexto](context-node-properties.md) .

Las propiedades de tipo cadena incluyen:

-   GUID \_ CNP \_ RECOGNIZEDSTRING
-   GUID \_ CNP \_ nombredeforma
-   GUID \_ AHP \_ ANALYSISHINTNAME
-   GUID \_ AHP \_ PREFIXTEXT
-   GUID \_ AHP \_ SUFFIXTEXT
-   GUID \_ AHP \_ FACTOID

El valor devuelto es ** \* WCHAR*_. Si convierte el parámetro \_ *ppbPropertyData* en **WCHAR \** ,_ la longitud devuelta es `(length of the string + 1) _ sizeof(WCHAR)` .

Las propiedades de tipo booleano incluyen:

-   GUID \_ AHP \_ OVERRIDELANGUAGEID
-   GUID \_ AHP \_ COERCETOFACTOID
-   GUID \_ AHP \_ WORDMODE

El valor devuelto es **Variant \_ bool**. Si convierte el parámetro \* *ppbPropertyData* en **Variant \_ bool \** _, la longitud devuelta es `sizeof(VARIANT_BOOL)` .

GUID \_ AHP \_ Guide es una propiedad de tipo guía. El valor devuelto _*es \* InkAnalysisRecognitionGuide*_. Si convierte el parámetro \_ *ppbPropertyData* en **InkAnalysisRecognitionGuide \** _, su longitud devuelta es `sizeof(InkAnalysisRecognitionGuide)` .

Las propiedades de tipo entero incluyen:

-   GUID \_ CNP \_ LINENUMBER
-   GUID \_ CNP \_ POINTSPERINCH
-   GUID \_ CNP \_ CONFIDENCELEVEL
-   \_confirmación de CNP de GUID \_
-   GUID \_ CNP \_ MAXIMUMSTROKECOUNT
-   \_segmentación de GUID CNP \_
-   GUID \_ CNP \_ ALIGNMENTLEVEL

El valor devuelto _*es \* Long*_. Si convierte el parámetro \_ *ppbPropertyData* en **Long \** _ la longitud devuelta es `sizeof(LONG)` .

Métricas de línea: las propiedades de tipo incluyen:

-   GUID \_ CNP \_ ascendente
-   GUID \_ CNP \_ descendente
-   \_línea base de CNP de GUID \_
-   CNP de GUID \_ \_

El valor devuelto _*es \* Long*_. Si convierte el parámetro \_ *ppbPropertyData* en **Long \** _ la longitud devuelta es, lo que indica `sizeof(LONG)_4` los valores (x, y) de los puntos de inicio seguidos de los valores (x, y) de los puntos finales.

GUID \_ CNP \_ TEXTRECOGNIZERID es una propiedad **GUID** . El valor devuelto es ** \* GUID*_. Si convierte el parámetro \_ *ppbPropertyData* en **GUID \** ,_ la longitud devuelta es `sizeof(GUID)` .

GUID \_ CNP \_ ROTATEDBOUNDINGBOX es una propiedad de rectángulo de selección rotado. El valor devuelto _*es \* Long*_. Si convierte el parámetro \_ *ppbPropertyData* en **\* Long* _ la longitud devuelta es, lo que significa que los `sizeof(LONG)_8` valores (x, y) de las cuatro esquinas del cuadro.

GUID \_ CNP \_ Hotpoint es una propiedad de punto de acceso frecuente. El valor devuelto es ** \* Long*_. Si convierte el parámetro \_ *ppbPropertyData* en **Long \**_ , la longitud devuelta es, lo que `sizeof(LONG)_2` significa los valores (x, y) para el punto.

GUID \_ AHP \_ lista de palabras es una propiedad de lista de palabras. El valor devuelto es ** \* WCHAR*_. Si convierte el parámetro \_ *ppbPropertyData* en **WCHAR \**_ , la longitud devuelta es `n _ sizeof(WCHAR)` , donde `n` es la suma de las longitudes de cadena del número de cadenas de la lista más 1 para cada carácter de terminación **null** para cada cadena.

## <a name="examples"></a>Ejemplos

Este ejemplo muestra un método que tiene acceso a la propiedad del nodo de contexto AlignmentLevel de un tipo de nodo de contexto de párrafo.


```C++
// Checks a paragraph context node's alignment level property.
// Only paragraph type context nodes contain the alignment level property.
HRESULT CMyClass::ExploreParagraphNode(
    IContextNode *pParagraphNode)
{
    // Get the AlignmentLevel property data for the paragraph.
    LONG * alignmentLevel = NULL;
    ULONG ulDataLen = 0;

    HRESULT hr = pParagraphNode->GetPropertyData(
        (const GUID*)&GUID_CNP_ALIGNMENTLEVEL,
        &ulDataLen,
        (BYTE**)&alignmentLevel);

    if( FAILED(hr) ||
        ulDataLen != sizeof(LONG) ||
        alignmentLevel == NULL )
    {
        // Insert code that handles an error here.
    }
    else
    {
        // Insert code that uses the alignment level here.
    }

    // Free the memory allocated for the property data.
    ::CoTaskMemFree(alignmentLevel);

    return hr;
}
```



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows XP Tablet PC Edition \[\]<br/>                                                 |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                                                     |
| Encabezado<br/>                   | <dl> <dt>IACom. h (también requiere IACom \_ i. c)</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>IACom.dll</dt> </dl>                          |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IContextNode**](icontextnode.md)
</dt> <dt>

[**IContextNode::AddPropertyData**](icontextnode-addpropertydata.md)
</dt> <dt>

[**IContextNode::RemovePropertyData**](icontextnode-removepropertydata.md)
</dt> <dt>

[**IContextNode::GetPropertyDataIds**](icontextnode-getpropertydataids.md)
</dt> <dt>

[**IContextNode::ContainsPropertyData**](icontextnode-containspropertydata.md)
</dt> <dt>

[**IContextNode::LoadPropertiesData**](icontextnode-loadpropertiesdata.md)
</dt> <dt>

[**IContextNode::SavePropertiesData**](icontextnode-savepropertiesdata.md)
</dt> <dt>

[Referencia de análisis de tinta](ink-analysis-reference.md)
</dt> </dl>

 

