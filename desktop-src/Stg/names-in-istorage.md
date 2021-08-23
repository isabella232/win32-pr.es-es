---
title: Nombres en IStorage
description: Un conjunto de propiedades se identifica con un identificador de formato (FMTID) en la interfaz IPropertySetStorage.
ms.assetid: 5f8eba37-c589-413e-9971-7ecb01dc6734
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e17b1125f642d3f24e24fa6040bc5e55ca3d48b2384aac551680b84c1496900f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119662385"
---
# <a name="names-in-istorage"></a>Nombres en IStorage

Un conjunto de propiedades se identifica con un identificador de formato (FMTID) en la [**interfaz IPropertySetStorage.**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) En la [**interfaz IStorage,**](/windows/desktop/api/Objidl/nn-objidl-istorage) un conjunto de propiedades se denomina con una cadena Unicode terminada en NULL con una longitud máxima de 32 caracteres. Para habilitar la interoperabilidad, se debe establecer una asignación entre fmtid y una cadena Unicode terminada en null correspondiente.

## <a name="converting-a-property-set-from-a-fmtid-to-a-string-name"></a>Convertir un conjunto de propiedades de FMTID en un nombre de cadena

Al convertir un FMTID en un nombre de cadena Unicode correspondiente, compruebe primero que FMTID es un valor conocido, que se muestra en la tabla siguiente. Si es así, use el nombre de cadena conocido correspondiente.

| FMTID                                                                                | Nombre de la cadena                       | Semántica                                                         |
|--------------------------------------------------------------------------------------|-----------------------------------|------------------------------------------------------------------|
| F29F85E0-4FF9-1068-AB91-08002B27B3D9                                                 | " \\ 005SummaryInformation"         | Información de resumen de COM2                                         |
| D5CDD502-2E9C-101B-9397-08002B2CF9AE D5CDD505-2E9C-101B-9397-08002B2CF9AE<br/> | " \\ 005DocumentSummaryInformation" | Office información de resumen del documento y propiedades definidas por el usuario. |



 

> [!Note]  
> El **conjunto de propiedades DocumentSummaryInformation** y **UserDefined** es único en que contiene dos secciones. No se permiten varias secciones en ningún otro conjunto de propiedades. Para obtener más información, vea [Structured Storage Serialized Property Set Format](structured-storage-serialized-property-set-format.md)y [DocumentSummaryInformation y UserDefined Property Sets](the-documentsummaryinformation-and-userdefined-property-sets.md). La primera sección se definió como parte de COM; el segundo se definió mediante Microsoft Office.

 

Si FMTID no es un valor conocido, use el siguiente procedimiento para formar un nombre de cadena de forma algorítmica.

**Para formar un nombre de cadena de forma algorítmica**

1.  Convierta fmtid en orden de bytes little-endian, si es necesario.
2.  Tome los 128 bits del FMTID y considélelos como una cadena de bits largos mediante la concatenación de cada uno de los bytes. El primer bit del valor de 128 bits es el bit menos significativo del primer byte en memoria del FMTID; el último bit del valor de 128 bits es el bit más significativo del último byte en memoria del FMTID. Extienda estos 128 bits a 130 bits agregando dos bits cero al final.
3.  Divida los 130 bits en grupos de cinco bits; habrá 26 grupos de este tipo. Considere cada grupo como un entero con prioridad de bits invertido. Por ejemplo, el primero de los 128 bits es el bit menos significativo del primer grupo de cinco bits; el quinto de los 128 bits es el bit más significativo del primer grupo.
4.  Asigne cada uno de estos enteros como un índice a la matriz de treinta y dos caracteres: ABCDEFJKLMNOPQRSTUVWXYZ012345. Esto produce una secuencia de 26 caracteres Unicode que usa solo caracteres en mayúsculas y números. No se aplican consideraciones que distinguen mayúsculas de minúsculas y que no distinguen mayúsculas de minúsculas, lo que hace que cada carácter sea único en cualquier configuración regional.
5.  Cree la cadena final concatenando la cadena "005" en la parte delantera de estos 26 caracteres, con una longitud total de \\ 27 caracteres.

En el código de ejemplo siguiente se muestra cómo asignar desde un FMTID a una cadena de propiedad.


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



## <a name="converting-a-property-set-from-a-string-name-to-a-fmtid"></a>Conversión de un conjunto de propiedades de un nombre de cadena a FMTID

Los convertidores de nombres de cadena de propiedad a GUID deben aceptar letras minúsculas como sinónimos de sus homólogos en mayúsculas.

En el código de ejemplo siguiente se muestra cómo asignar desde una cadena de propiedad a un FMTID.


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



Al intentar abrir un conjunto de propiedades existente, en [IPropertySetStorage::Open](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-open), fmtid (raíz) se convierte en una cadena como se describió anteriormente. Si existe un elemento [**de IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) de ese nombre, se usa. De lo contrario, se produce un error en la apertura.

Al crear un nuevo conjunto de propiedades, la asignación anterior determina el nombre de cadena utilizado.

 

 





