---
description: Recupera datos específicos de la aplicación u otros datos de propiedad para el identificador especificado.
ms.assetid: eaf95ff8-7b31-4c05-aa49-0c3bb9e996c0
title: Método IContextNode::GetPropertyData (IACom.h)
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
ms.openlocfilehash: 89e7ab9fb5213b41d53695b516b95b47193e8d803b207efd09216c743085927e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119660743"
---
# <a name="icontextnodegetpropertydata-method"></a>IContextNode::GetPropertyData (método)

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

*pPropertyDataId* \[ En\]
</dt> <dd>

Identificador de los datos.

</dd> <dt>

*pulPropertyDataSize* \[ in, out\]
</dt> <dd>

Tamaño de los datos en bytes. No se usa el valor que se pasa.

</dd> <dt>

*ppbPropertyData* \[ out\]
</dt> <dd>

Puntero a una matriz de enteros de 8 bits sin signo que contiene los datos de propiedad.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Para obtener una descripción de los valores [devueltos, vea Clases e interfaces: análisis de entrada de lápiz.](classes-and-interfaces---ink-analysis.md)

## <a name="remarks"></a>Comentarios

> [!Caution]  
> Para evitar una pérdida de memoria, use [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree) para liberar la memoria de \* *ppbPropertyData* cuando ya no necesite la información.

 

Además de recuperar datos específicos de la aplicación que se agregaron con [**IContextNode::AddPropertyData,**](icontextnode-addpropertydata.md)este método se usa para recuperar las propiedades comunes descritas por las constantes Propiedades del nodo [de](context-node-properties.md) contexto.

Las propiedades de tipo cadena incluyen:

-   GUID \_ CNP \_ RECOGNIZEDSTRING
-   GUID \_ CNP \_ SHAPENAME
-   GUID \_ AHP \_ ANALYSISHINTNAME
-   GUID \_ AHP \_ PREFIXTEXT
-   GUID \_ AHP \_ SUFFIXTEXT
-   GUID \_ AHP \_ FACTOID

El valor devuelto es **WCHAR. \**_Si convierte el parámetro \_ *ppbPropertyData* en **WCHAR, \**_ su longitud devuelta es `(length of the string + 1) _ sizeof(WCHAR)` .

Las propiedades de tipo booleano incluyen:

-   GUID \_ AHP \_ OVERRIDELANGUAGEID
-   GUID \_ AHP \_ COERCETOFACTOID
-   GUID \_ AHP \_ WORDMODE

El valor devuelto es **VARIANT \_ BOOL.** Si convierte el parámetro \* *ppbPropertyData* a **VARIANT \_ BOOL, \*** su longitud devuelta es `sizeof(VARIANT_BOOL)` .

GUID \_ AHP \_ GUIDE es una propiedad de tipo de guía. El valor devuelto es **InkAnalysisRecognitionGuide \** _. Si convierte el parámetro \_ *ppbPropertyData* en **InkAnalysisRecognitionGuide, \*** su longitud devuelta es `sizeof(InkAnalysisRecognitionGuide)` .

Las propiedades de tipo entero incluyen:

-   GUID \_ CNP \_ LINENUMBER
-   GUID \_ CNP \_ POINTSPERINCH
-   GUID \_ CNP \_ CONFIDENCELEVEL
-   CONFIRMACIÓN \_ DE CNP \_ DE GUID
-   GUID \_ CNP \_ MAXIMUMSTROKECOUNT
-   SEGMENTACIÓN \_ DE CNP \_ GUID
-   GUID \_ CNP \_ ALIGNMENTLEVEL

El valor devuelto es **LONG \** _. Si convierte el parámetro \_ *ppbPropertyData* en **LONG, \*** su longitud devuelta es `sizeof(LONG)` .

Las propiedades de tipo de métricas de línea incluyen:

-   ASCENDENTES \_ DE CNP \_ GUID
-   DESCENDIENTES \_ DE CNP \_ GUID
-   LÍNEA BASE \_ DE CNP \_ GUID
-   GUID \_ CNP \_ MIDLINE

El valor devuelto es **\* LONG.*_Si convierte el parámetro \_ *ppbPropertyData* en **LONG, \**_ su longitud devuelta es , lo que significa los valores (x, y) de los puntos iniciales seguidos de los valores (x, y) para los puntos `sizeof(LONG)_4` finales.

GUID \_ CNP \_ TEXTRECOGNIZERID es una **propiedad GUID.** El valor devuelto es **GUID \** _. Si convierte el parámetro \_ *ppbPropertyData* al **GUID, \*** su longitud devuelta es `sizeof(GUID)` .

GUID \_ CNP \_ ROTATEDBOUNDINGBOX es una propiedad de cuadro de límite girado. El valor devuelto es **\* LONG.*_Si convierte el parámetro \_ *ppbPropertyData* en **LONG, \**_ su longitud devuelta es , lo que significa los valores (x, y) de las cuatro esquinas `sizeof(LONG)_8` del cuadro.

\_CNP \_ HOTPOINT GUID es una propiedad de punto de acceso. El valor devuelto es **\* LONG.*_Si convierte el parámetro \_ *ppbPropertyData* en **LONG, \**_ su longitud devuelta es , lo que significa los `sizeof(LONG)_2` valores (x, y) del punto.

GUID \_ AHP \_ WORDLIST es una propiedad de lista de palabras. El valor devuelto es **WCHAR. \**_Si convierte el parámetro \_ *ppbPropertyData* en **WCHAR, \**_ su longitud devuelta es , donde es la suma de las longitudes de cadena del número de cadenas de la lista más 1 para cada carácter de terminación NULL para `n _ sizeof(WCHAR)` cada `n` cadena. 

## <a name="examples"></a>Ejemplos

En este ejemplo se muestra un método que tiene acceso a la propiedad de nodo de contexto AlignmentLevel de un tipo de nodo de contexto Paragraph.


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



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de XP Tablet PC \[ Edition\]<br/>                                                 |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                                                     |
| Header<br/>                   | <dl> <dt>IACom.h (también requiere IACom \_ i.c)</dt> </dl> |
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

[Referencia de análisis de entrada de lápiz](ink-analysis-reference.md)
</dt> </dl>

 

