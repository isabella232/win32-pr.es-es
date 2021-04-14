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
# <a name="names-in-istorage"></a>Nombres en IStorage

Un conjunto de propiedades se identifica con un identificador de formato (FMTID) en la interfaz [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) . En la interfaz [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) , se asigna un nombre a un conjunto de propiedades con una cadena Unicode terminada en NULL con una longitud máxima de 32 caracteres. Para habilitar la interoperabilidad, se debe establecer una asignación entre un FMTID y una cadena Unicode terminada en NULL correspondiente.

## <a name="converting-a-property-set-from-a-fmtid-to-a-string-name"></a>Convertir un conjunto de propiedades de FMTID en un nombre de cadena

Al convertir de una FMTID a un nombre de cadena Unicode correspondiente, compruebe primero que FMTID es un valor conocido, que se muestra en la tabla siguiente. Si es así, use el nombre de cadena conocido correspondiente.

| FMTID                                                                                | Nombre de la cadena                       | Semántica                                                         |
|--------------------------------------------------------------------------------------|-----------------------------------|------------------------------------------------------------------|
| F29F85E0-4FF9-1068-AB91-08002B27B3D9                                                 | " \\ 005SummaryInformation"         | Información de Resumen de COM2                                         |
| D5CDD502-2E9C-101B-9397-08002B2CF9AE D5CDD505-2E9C-101B-9397-08002B2CF9AE<br/> | " \\ 005DocumentSummaryInformation" | Información de resumen del documento de Office y propiedades definidas por el usuario. |



 

> [!Note]  
> El conjunto de propiedades **DocumentSummaryInformation** y **UserDefined** es único en que contiene dos secciones. No se permiten varias secciones en ningún otro conjunto de propiedades. Para obtener más información, vea [formato del conjunto de propiedades serializado de almacenamiento estructurado](structured-storage-serialized-property-set-format.md)y [los conjuntos de propiedades DocumentSummaryInformation y UserDefined](the-documentsummaryinformation-and-userdefined-property-sets.md). La primera sección se definió como parte de COM; la segunda se definió mediante Microsoft Office.

 

Si FMTID no es un valor conocido, use el procedimiento siguiente para formar un nombre de cadena de forma algorítmica.

**Para formar un nombre de cadena de forma algorítmica**

1.  Convierta FMTID en un orden de bytes Little-endian, si es necesario.
2.  Tome los 128 bits de FMTID y considérelos como una cadena de bit largo mediante la concatenación de cada uno de los bytes juntos. El primer bit del valor de bit 128 es el bit menos significativo del primer byte de la memoria de FMTID; el último bit del valor de 128 bits es el bit más significativo del último byte de la memoria de FMTID. Extienda estos 128 bits a 130 bits agregando dos bits cero al final.
3.  Divida los bits 130 en grupos de cinco bits; habrá 26 grupos de este tipo. Considere cada grupo como un entero con precedencia de bits inverso. Por ejemplo, el primero de los bits 128 es el bit menos significativo del primer grupo de cinco bits; la quinta parte de los 128 bits es el bit más significativo del primer grupo.
4.  Asigne cada uno de estos enteros como un índice en la matriz de 32 caracteres: ABCDEFGHIJKLMNOPQRSTUVWXYZ012345. Esto produce una secuencia de 26 caracteres Unicode que solo usa caracteres en mayúsculas y números. No se aplican consideraciones que distinguen mayúsculas de minúsculas y no distinguen mayúsculas de minúsculas, lo que hace que cada carácter sea único en cualquier configuración regional.
5.  Cree la cadena final mediante la concatenación de la cadena " \\ 005" en la parte delantera de estos 26 caracteres, con una longitud total de 27 caracteres.

En el ejemplo de código siguiente se muestra cómo asignar un FMTID a una cadena de propiedad.


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



## <a name="converting-a-property-set-from-a-string-name-to-a-fmtid"></a>Convertir un conjunto de propiedades de un nombre de cadena en un FMTID

Los convertidores de nombres de cadena de propiedad en GUID deben aceptar letras minúsculas como sinónimos de sus homólogos en mayúsculas.

En el ejemplo de código siguiente se muestra cómo asignar desde una cadena de propiedad a un FMTID.


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



Al intentar abrir un conjunto de propiedades existente, en [IPropertySetStorage:: Open](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-open), el FMTID (raíz) se convierte en una cadena, tal y como se ha descrito anteriormente. Si existe un elemento con el [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) de ese nombre, se utiliza. De lo contrario, se produce un error en Open.

Al crear un nuevo conjunto de propiedades, la asignación anterior determina el nombre de la cadena que se usa.

 

 





