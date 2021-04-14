---
title: Nombres en IStorage
description: Un conjunto de propiedades se identifica con un identificador de formato (FMTID) en la interfaz IPropertySetStorage.
ms.assetid: 5f8eba37-c589-413e-9971-7ecb01dc6734
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6cef9417f2f5fad7fd17dcc3d431f1d3565a3843
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104532494"
---
# <a name="names-in-istorage"></a><span data-ttu-id="18796-103">Nombres en IStorage</span><span class="sxs-lookup"><span data-stu-id="18796-103">Names in IStorage</span></span>

<span data-ttu-id="18796-104">Un conjunto de propiedades se identifica con un identificador de formato (FMTID) en la interfaz [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) .</span><span class="sxs-lookup"><span data-stu-id="18796-104">A property set is identified with a format identifier (FMTID) in the [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) interface.</span></span> <span data-ttu-id="18796-105">En la interfaz [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) , se asigna un nombre a un conjunto de propiedades con una cadena Unicode terminada en NULL con una longitud máxima de 32 caracteres.</span><span class="sxs-lookup"><span data-stu-id="18796-105">In the [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) interface, a property set is named with a null-terminated Unicode string with a maximum length of 32 characters.</span></span> <span data-ttu-id="18796-106">Para habilitar la interoperabilidad, se debe establecer una asignación entre un FMTID y una cadena Unicode terminada en NULL correspondiente.</span><span class="sxs-lookup"><span data-stu-id="18796-106">To enable interoperability, a mapping between an FMTID and a corresponding null-terminated Unicode string must be established.</span></span>

## <a name="converting-a-property-set-from-a-fmtid-to-a-string-name"></a><span data-ttu-id="18796-107">Convertir un conjunto de propiedades de FMTID en un nombre de cadena</span><span class="sxs-lookup"><span data-stu-id="18796-107">Converting a property set from a FMTID to a string name</span></span>

<span data-ttu-id="18796-108">Al convertir de una FMTID a un nombre de cadena Unicode correspondiente, compruebe primero que FMTID es un valor conocido, que se muestra en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="18796-108">When converting from an FMTID to a corresponding Unicode string name, first verify that the FMTID is a well-known value, listed in the following table.</span></span> <span data-ttu-id="18796-109">Si es así, use el nombre de cadena conocido correspondiente.</span><span class="sxs-lookup"><span data-stu-id="18796-109">If so, then use the corresponding well-known string name.</span></span>

| <span data-ttu-id="18796-110">FMTID</span><span class="sxs-lookup"><span data-stu-id="18796-110">FMTID</span></span>                                                                                | <span data-ttu-id="18796-111">Nombre de la cadena</span><span class="sxs-lookup"><span data-stu-id="18796-111">String name</span></span>                       | <span data-ttu-id="18796-112">Semántica</span><span class="sxs-lookup"><span data-stu-id="18796-112">Semantic</span></span>                                                         |
|--------------------------------------------------------------------------------------|-----------------------------------|------------------------------------------------------------------|
| <span data-ttu-id="18796-113">F29F85E0-4FF9-1068-AB91-08002B27B3D9</span><span class="sxs-lookup"><span data-stu-id="18796-113">F29F85E0-4FF9-1068-AB91-08002B27B3D9</span></span>                                                 | <span data-ttu-id="18796-114">" \\ 005SummaryInformation"</span><span class="sxs-lookup"><span data-stu-id="18796-114">"\\005SummaryInformation"</span></span>         | <span data-ttu-id="18796-115">Información de Resumen de COM2</span><span class="sxs-lookup"><span data-stu-id="18796-115">COM2 summary information</span></span>                                         |
| <span data-ttu-id="18796-116">D5CDD502-2E9C-101B-9397-08002B2CF9AE D5CDD505-2E9C-101B-9397-08002B2CF9AE</span><span class="sxs-lookup"><span data-stu-id="18796-116">D5CDD502-2E9C-101B-9397-08002B2CF9AE D5CDD505-2E9C-101B-9397-08002B2CF9AE</span></span><br/> | <span data-ttu-id="18796-117">" \\ 005DocumentSummaryInformation"</span><span class="sxs-lookup"><span data-stu-id="18796-117">"\\005DocumentSummaryInformation"</span></span> | <span data-ttu-id="18796-118">Información de resumen del documento de Office y propiedades definidas por el usuario.</span><span class="sxs-lookup"><span data-stu-id="18796-118">Office document summary information and user-defined properties.</span></span> |



 

> [!Note]  
> <span data-ttu-id="18796-119">El conjunto de propiedades **DocumentSummaryInformation** y **UserDefined** es único en que contiene dos secciones.</span><span class="sxs-lookup"><span data-stu-id="18796-119">The **DocumentSummaryInformation** and **UserDefined** property set is unique in that it contains two sections.</span></span> <span data-ttu-id="18796-120">No se permiten varias secciones en ningún otro conjunto de propiedades.</span><span class="sxs-lookup"><span data-stu-id="18796-120">Multiple sections are not permitted in any other property set.</span></span> <span data-ttu-id="18796-121">Para obtener más información, vea [formato del conjunto de propiedades serializado de almacenamiento estructurado](structured-storage-serialized-property-set-format.md)y [los conjuntos de propiedades DocumentSummaryInformation y UserDefined](the-documentsummaryinformation-and-userdefined-property-sets.md).</span><span class="sxs-lookup"><span data-stu-id="18796-121">For more information, see [Structured Storage Serialized Property Set Format](structured-storage-serialized-property-set-format.md), and [The DocumentSummaryInformation and UserDefined Property Sets](the-documentsummaryinformation-and-userdefined-property-sets.md).</span></span> <span data-ttu-id="18796-122">La primera sección se definió como parte de COM; la segunda se definió mediante Microsoft Office.</span><span class="sxs-lookup"><span data-stu-id="18796-122">The first section was defined as part of COM; the second was defined by Microsoft Office.</span></span>

 

<span data-ttu-id="18796-123">Si FMTID no es un valor conocido, use el procedimiento siguiente para formar un nombre de cadena de forma algorítmica.</span><span class="sxs-lookup"><span data-stu-id="18796-123">If the FMTID is not a well-known value, then use the following procedure to algorithmically form a string name.</span></span>

<span data-ttu-id="18796-124">**Para formar un nombre de cadena de forma algorítmica**</span><span class="sxs-lookup"><span data-stu-id="18796-124">**To algorithmically form a string name**</span></span>

1.  <span data-ttu-id="18796-125">Convierta FMTID en un orden de bytes Little-endian, si es necesario.</span><span class="sxs-lookup"><span data-stu-id="18796-125">Convert the FMTID to little-endian byte order, if necessary.</span></span>
2.  <span data-ttu-id="18796-126">Tome los 128 bits de FMTID y considérelos como una cadena de bit largo mediante la concatenación de cada uno de los bytes juntos.</span><span class="sxs-lookup"><span data-stu-id="18796-126">Take the 128 bits of the FMTID and consider them as one long bit string by concatenating each of the bytes together.</span></span> <span data-ttu-id="18796-127">El primer bit del valor de bit 128 es el bit menos significativo del primer byte de la memoria de FMTID; el último bit del valor de 128 bits es el bit más significativo del último byte de la memoria de FMTID.</span><span class="sxs-lookup"><span data-stu-id="18796-127">The first bit of the 128 bit value is the least significant bit of the first byte in memory of the FMTID; the last bit of the 128 bit value is the most significant bit of the last byte in memory of the FMTID.</span></span> <span data-ttu-id="18796-128">Extienda estos 128 bits a 130 bits agregando dos bits cero al final.</span><span class="sxs-lookup"><span data-stu-id="18796-128">Extend these 128 bits to 130 bits by adding two zero bits to the end.</span></span>
3.  <span data-ttu-id="18796-129">Divida los bits 130 en grupos de cinco bits; habrá 26 grupos de este tipo.</span><span class="sxs-lookup"><span data-stu-id="18796-129">Divide the 130 bits into groups of five bits; there will be 26 such groups.</span></span> <span data-ttu-id="18796-130">Considere cada grupo como un entero con precedencia de bits inverso.</span><span class="sxs-lookup"><span data-stu-id="18796-130">Consider each group as an integer with reversed bit precedence.</span></span> <span data-ttu-id="18796-131">Por ejemplo, el primero de los bits 128 es el bit menos significativo del primer grupo de cinco bits; la quinta parte de los 128 bits es el bit más significativo del primer grupo.</span><span class="sxs-lookup"><span data-stu-id="18796-131">For example, the first of the 128 bits is the least significant bit of the first group of five bits; the fifth of the 128 bits is the most significant bit of the first group.</span></span>
4.  <span data-ttu-id="18796-132">Asigne cada uno de estos enteros como un índice en la matriz de 32 caracteres: ABCDEFGHIJKLMNOPQRSTUVWXYZ012345.</span><span class="sxs-lookup"><span data-stu-id="18796-132">Map each of these integers as an index into the array of thirty-two characters: ABCDEFGHIJKLMNOPQRSTUVWXYZ012345.</span></span> <span data-ttu-id="18796-133">Esto produce una secuencia de 26 caracteres Unicode que solo usa caracteres en mayúsculas y números.</span><span class="sxs-lookup"><span data-stu-id="18796-133">This yields a sequence of 26 Unicode characters that uses only uppercase characters and numerals.</span></span> <span data-ttu-id="18796-134">No se aplican consideraciones que distinguen mayúsculas de minúsculas y no distinguen mayúsculas de minúsculas, lo que hace que cada carácter sea único en cualquier configuración regional.</span><span class="sxs-lookup"><span data-stu-id="18796-134">Case sensitive and case insensitive considerations do not apply, causing each character to be unique in any locale.</span></span>
5.  <span data-ttu-id="18796-135">Cree la cadena final mediante la concatenación de la cadena " \\ 005" en la parte delantera de estos 26 caracteres, con una longitud total de 27 caracteres.</span><span class="sxs-lookup"><span data-stu-id="18796-135">Create the final string by concatenating the string "\\005" onto the front of these 26 characters, for a total length of 27 characters.</span></span>

<span data-ttu-id="18796-136">En el ejemplo de código siguiente se muestra cómo asignar un FMTID a una cadena de propiedad.</span><span class="sxs-lookup"><span data-stu-id="18796-136">The following example code shows how to map from an FMTID to a property string.</span></span>


```C++
#define CBIT_BYTE        8
#define CBIT_CHARMASK    5
#define CCH_MAP          (1 << CBIT_CHARMASK)    // 32
#define CHARMASK         (CCH_MAP - 1)           // 0x1f
 
CHAR awcMap[CCH_MAP + 1] = "abcdefghijklmnopqrstuvwxyz012345";
 
WCHAR MapChar(ULONG I) {
    return((WCHAR) awcMap[i & CHARMASK]);
    }
 
VOID GuidToPropertyStringName(GUID *pguid, WCHAR awcname[]) {
    BYTE *pb = (BYTE *) pguid;
    BYTE *pbEnd = pb + sizeof(*pguid);
    ULONG cbitRemain = CBIT_BYTE;
    WCHAR *pwc = awcname;
 
    *pwc++ = ((WCHAR) 0x0005);
    while (pb < pbEnd) {
        ULONG i = *pb >> (CBIT_BYTE - cbitRemain);
        if (cbitRemain >= CBIT_CHARMASK) {
            *pwc = MapChar(i);
            if (cbitRemain == CBIT_BYTE && 
                                    *pwc >= L'a' && *pwc <= L'z')
                {
                *pwc += (WCHAR) (L'A' - L'a');
                }
            pwc++;
            cbitRemain -= CBIT_CHARMASK;
            if (cbitRemain == 0) {
                pb++;
                cbitRemain = CBIT_BYTE;
                }
            }
        else {
            if (++pb < pbEnd) {
                i |= *pb << cbitRemain;
                }
            *pwc++ = MapChar(i);
            cbitRemain += CBIT_BYTE - CBIT_CHARMASK;
            }
        }
    *pwc = L'\0';
    }
```



## <a name="converting-a-property-set-from-a-string-name-to-a-fmtid"></a><span data-ttu-id="18796-137">Convertir un conjunto de propiedades de un nombre de cadena en un FMTID</span><span class="sxs-lookup"><span data-stu-id="18796-137">Converting a property set from a string name to a FMTID</span></span>

<span data-ttu-id="18796-138">Los convertidores de nombres de cadena de propiedad en GUID deben aceptar letras minúsculas como sinónimos de sus homólogos en mayúsculas.</span><span class="sxs-lookup"><span data-stu-id="18796-138">Converters of property string names to GUIDs should accept lowercase letters as synonymous with their uppercase counterparts.</span></span>

<span data-ttu-id="18796-139">En el ejemplo de código siguiente se muestra cómo asignar desde una cadena de propiedad a un FMTID.</span><span class="sxs-lookup"><span data-stu-id="18796-139">The following example code shows how to map from a property string to an FMTID.</span></span>


```C++
#include "stdafx.h"
#define _INC_OLE
#include <windows.h>
#include <stdlib.h>
#include <stdio.h>
#include <string.h>
#include <ctype.h>
#define CBIT_CHARMASK 5
#define CBIT_BYTE     8
#define CBIT_GUID    (CBIT_BYTE * sizeof(GUID))
#define CWC_PROPSET  (1 + (CBIT_GUID + CBIT_CHARMASK-1)/CBIT_CHARMASK)
#define WC_PROPSET0  ((WCHAR) 0x0005)
#define CCH_MAP      (1 << CBIT_CHARMASK)        // 32
#define CHARMASK     (CCH_MAP - 1)            // 0x1f
CHAR awcMap[CCH_MAP + 1] = "abcdefghijklmnopqrstuvwxyz012345";
#define CALPHACHARS  ('z' - 'a' + 1)

GUID guidSummary =
{ 0xf29f85e0,0x4ff9, 0x1068,
{ 0xab, 0x91, 0x08, 0x00, 0x2b, 0x27, 0xb3, 0xd9 } };

WCHAR wszSummary[] = L"SummaryInformation";

GUID guidDocumentSummary =
    { 0xd5cdd502,
      0x2e9c, 0x101b,
      { 0x93, 0x97, 0x08, 0x00, 0x2b, 0x2c, 0xf9, 0xae } };

WCHAR wszDocumentSummary[] = L"DocumentSummaryInformation";
__inline WCHAR

MapChar(IN ULONG i)
{
    return((WCHAR) awcMap[i & CHARMASK]);
}

ULONG PropertySetNameToGuid(
    IN ULONG cwcname,
    IN WCHAR const awcname[],
    OUT GUID *pguid)
{
    ULONG Status = ERROR_INVALID_PARAMETER;
    WCHAR const *pwc = awcname;

    if (pwc[0] == WC_PROPSET0)
    {
        //Note: cwcname includes the WC_PROPSET0, and
        //sizeof(wsz...) includes the trailing L'\0', but
        //the comparison excludes both the leading
        //WC_PROPSET0 and the trailing L'\0'.
        if (cwcname == sizeof(wszSummary)/sizeof(WCHAR) &&
            wcsnicmp(&pwc[1], wszSummary, cwcname - 1) == 0)
        {
            *pguid = guidSummary;
            return(NO_ERROR);
        }
        if (cwcname == CWC_PROPSET)
        {
            ULONG cbit;
            BYTE *pb = (BYTE *) pguid - 1;
            ZeroMemory(pguid, sizeof(*pguid));
            for (cbit = 0; cbit < CBIT_GUID; cbit += 
            CBIT_CHARMASK)
            {
                ULONG cbitUsed = cbit % CBIT_BYTE;
                ULONG cbitStored;
                WCHAR wc;
                if (cbitUsed == 0)
                {
                    pb++;
                }
                wc = *++pwc - L'A';        //assume uppercase
                if (wc > CALPHACHARS)
                {
                    wc += (WCHAR) (L'A' - L'a'); //try lowercase
                    if (wc > CALPHACHARS)
                    {
                        wc += L'a' - L'0' + CALPHACHARS; 
                        if (wc > CHARMASK)
                        {
                            goto fail;       //invalid character
                        }
                    }
                }
                *pb |= (BYTE) (wc << cbitUsed);
                cbitStored = min(CBIT_BYTE - cbitUsed, 
                CBIT_CHARMASK);

                //If the translated bits will not fit in the 
                //current byte
                if (cbitStored < CBIT_CHARMASK)
                {
                    wc >>= CBIT_BYTE - cbitUsed;
                    if (cbit + cbitStored == CBIT_GUID)
                    {
                       if (wc != 0)
                       {
                           goto fail;        //extra bits
                       }
                       break;
                    }
                    pb++;
                    *pb |= (BYTE) wc;
                }
           }
           Status = NO_ERROR;
      }
    }
fail:
    return(Status);
}
```



<span data-ttu-id="18796-140">Al intentar abrir un conjunto de propiedades existente, en [IPropertySetStorage:: Open](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-open), el FMTID (raíz) se convierte en una cadena, tal y como se ha descrito anteriormente.</span><span class="sxs-lookup"><span data-stu-id="18796-140">When attempting to open an existing property set, in [IPropertySetStorage::Open](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-open), the (root) FMTID is converted to a string as described above.</span></span> <span data-ttu-id="18796-141">Si existe un elemento con el [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) de ese nombre, se utiliza.</span><span class="sxs-lookup"><span data-stu-id="18796-141">If an element of the [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) of that name exists, it is used.</span></span> <span data-ttu-id="18796-142">De lo contrario, se produce un error en Open.</span><span class="sxs-lookup"><span data-stu-id="18796-142">Otherwise, the open fails.</span></span>

<span data-ttu-id="18796-143">Al crear un nuevo conjunto de propiedades, la asignación anterior determina el nombre de la cadena que se usa.</span><span class="sxs-lookup"><span data-stu-id="18796-143">When creating a new property set, the above mapping determines the string name used.</span></span>

 

 





