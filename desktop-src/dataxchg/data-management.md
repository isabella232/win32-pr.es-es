---
title: Administración de datos
description: En este tema se describe cómo los objetos de memoria pasan datos de una aplicación a otra.
ms.assetid: 32919f27-4699-4831-8837-c5160b1daf4e
keywords:
- Interfaz de usuario de Windows, Intercambio dinámico de datos (DDE)
- Intercambio dinámico de datos (DDE), administración de datos
- DDE (Intercambio dinámico de datos), administración de datos
- intercambio de datos, Intercambio dinámico de datos (DDE)
- Interfaz de usuario de Windows, biblioteca de administración de Intercambio dinámico de datos (DDEML)
- Biblioteca de administración de Intercambio dinámico de datos (DDEML), administración de datos
- DDEML (biblioteca de administración de Intercambio dinámico de datos), administración de datos
- intercambio de datos, biblioteca de administración de Intercambio dinámico de datos (DDEML)
- Intercambio dinámico de datos (DDE), objetos
- DDE (Intercambio dinámico de datos), objetos
- Biblioteca de administración de Intercambio dinámico de datos (DDEML), objetos
- DDEML (biblioteca de administración de Intercambio dinámico de datos), objetos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dfc5178f636cf4b75111d4fc48e17fd144400a91
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104419162"
---
# <a name="data-management"></a>Administración de datos

Dado que Intercambio dinámico de datos (DDE) utiliza objetos de memoria para pasar datos de una aplicación a otra, la biblioteca de administración de Intercambio dinámico de datos (DDEML) proporciona un conjunto de funciones que las aplicaciones DDE pueden utilizar para crear y administrar objetos DDE.

Todas las transacciones que implican el intercambio de datos requieren que la aplicación proporcione los datos para crear un búfer local que contenga los datos y, a continuación, llamar a la función [**DdeCreateDataHandle**](/windows/desktop/api/Ddeml/nf-ddeml-ddecreatedatahandle) . Esta función asigna un objeto DDE, copia los datos del búfer al objeto y devuelve un identificador de datos. Un identificador de datos es un valor **DWORD** que el ddeml usa para proporcionar acceso a los datos del objeto DDE. Para compartir los datos en un objeto DDE, una aplicación pasa el identificador de datos a DDEML y el DDEML pasa el identificador a la función de devolución de llamada DDE de la aplicación que recibe la transacción de datos.

En el ejemplo siguiente se muestra cómo crear un objeto DDE y cómo obtener un identificador para el objeto. Durante la transacción [**XTYP \_ ADVREQ**](xtyp-advreq.md) , la función de devolución de llamada convierte la hora actual en una cadena ASCII, copia la cadena en un búfer local y, a continuación, crea un objeto DDE que contiene la cadena. La función de devolución de llamada devuelve el identificador del objeto DDE (HDDEDATA) a DDEML, que pasa el identificador a la aplicación cliente.


```
typedef struct tagTIME 
{ 
    INT     hour;   // 0 - 11 hours for analog clock 
    INT     hour12; // 12-hour format 
    INT     hour24; // 24-hour format 
    INT     minute; 
    INT     second; 
    INT     ampm;   // 0 - AM , 1 - PM 
} TIME; 
 
HDDEDATA EXPENTRY DdeCallback(uType, uFmt, hconv, hsz1, hsz2, 
    hdata, dwData1, dwData2) 
UINT uType; 
UINT uFmt; 
HCONV hconv; 
HSZ hsz1; 
HSZ hsz2; 
HDDEDATA hdata; 
DWORD dwData1; 
DWORD dwData2; 
{ 
 
    CHAR szBuf[32];
    HRESULT hResult;
    size_t * pcch;
    HRESULT hResult; 
 
    switch (uType) 
    { 
    case XTYP_ADVREQ: 
        if ((hsz1 == hszTime && hsz2 == hszNow) && 
                (uFmt == CF_TEXT)) 
        { 
            // Copy the formatted string to a buffer. 
 
            itoa(tmTime.hour, szBuf, 10);
            hResult = StringCchCat(szBuf, 32/sizeof(TCHAR), ":"); 
            if (FAILED(hResult))
            {
            // TO DO: Write error handler.
                return;
            }
            if (tmTime.minute < 10)
                hResult = StringCchCat(szBuf, 32/sizeof(TCHAR), "0"); 
                if (FAILED(hResult)
            {
            // TO DO: Write error handler.
                return;
            } 
            hResult = StringCchLength(szBuf, 32/sizeof(TCHAR), pcch);
            if (FAILED(hResult))
            {
            // TO DO: Write error handler.
                return;
            }
            itoa(tmTime.minute, &szBuf[*pcch], 10);
            hResult = StringCchCat(szBuf, 32/sizeof(TCHAR), ":"); 
            if (FAILED(hResult)
            {
            // TO DO: Write error handler.
                return;
            }
            if (tmTime.second < 10) 
                hResult = StringCchCat(szBuf, 32/sizeof(TCHAR), "0"); 
            if (FAILED(hResult)
            {
            // TO DO: Write error handler.
                return;
            }
            hResult = StringCchLength(szBuf, 32/sizeof(TCHAR), pcch);
            if (FAILED(hResult))
            {
            // TO DO: Write error handler.
                return;
            }
            itoa(tmTime.second, &szBuf[*pcch], 10);
            hResult = StringCchLength(szBuf, 32/sizeof(TCHAR), pcch);
            if (FAILED(hResult))
            {
            // TO DO: Write error handler.
                return;
            } 
            szBuf[*pcch] = '\0'; 
 
            // Create a global object and return its data handle. 
            hResult = StringCchLength(szBuf, 32/sizeof(TCHAR), pcch);
            if (FAILED(hResult))
            {
            // TO DO: Write error handler.
                return;
            }
            return (DdeCreateDataHandle( 
                idInst, 
                (LPBYTE) szBuf,     // instance identifier 
                *pcch + 1,          // source buffer length 
                0,                  // offset from beginning 
                hszNow,             // item name string 
                CF_TEXT,            // clipboard format 
                0));                // no creation flags 
        } else return (HDDEDATA) NULL; 
 
    // Process other transactions. 
    } 
} 
```



La aplicación receptora obtiene un puntero al objeto DDE pasando el identificador de datos a la función [**DdeAccessData**](/windows/desktop/api/Ddeml/nf-ddeml-ddeaccessdata) . El puntero devuelto por **DdeAccessData** proporciona acceso de solo lectura. La aplicación debe usar el puntero para revisar los datos y, a continuación, llamar a la función [**DdeUnaccessData**](/windows/desktop/api/Ddeml/nf-ddeml-ddeunaccessdata) para invalidar el puntero. La aplicación puede copiar los datos en un búfer local mediante la función [**DdeGetData**](/windows/desktop/api/Ddeml/nf-ddeml-ddegetdata) .

En el ejemplo siguiente se obtiene un puntero al objeto DDE identificado por el parámetro *hData* , se copia el contenido en un búfer local y, a continuación, se invalida el puntero.


```
HDDEDATA hdata; 
LPBYTE lpszAdviseData; 
DWORD cbDataLen; 
DWORD i; 
char szData[32]; 
 
// 
case XTYP_ADVDATA: 
    lpszAdviseData = DdeAccessData(hdata, &cbDataLen); 
    for (i = 0; i < cbDataLen; i++) 
        szData[i] = *lpszAdviseData++; 
    DdeUnaccessData(hdata); 
    return (HDDEDATA) TRUE; 
//
```



Normalmente, cuando una aplicación que creó un identificador de datos pasa ese identificador a DDEML, el identificador deja de ser válido en la aplicación que se crea. Esta situación no es un problema si la aplicación debe compartir datos con una sola aplicación. Sin embargo, si una aplicación debe compartir los mismos datos con varias aplicaciones, la aplicación que crea debe especificar la \_ marca HDATA APPOWNED en [**DdeCreateDataHandle**](/windows/desktop/api/Ddeml/nf-ddeml-ddecreatedatahandle). Al hacerlo, se proporciona la propiedad del objeto DDE a la aplicación de creación y se impide que DDEML invalide el identificador de datos. A continuación, la aplicación puede pasar el identificador de datos cualquier número de veces después de llamar a **DdeCreateDataHandle** solo una vez.

Si una aplicación especifica la \_ marca HDATA APPOWNED en el parámetro *AfCmd* de [**DdeCreateDataHandle**](/windows/desktop/api/Ddeml/nf-ddeml-ddecreatedatahandle), debe llamar a la función [**DdeFreeDataHandle**](/windows/desktop/api/Ddeml/nf-ddeml-ddefreedatahandle) para liberar el identificador de memoria, independientemente de si pasó el identificador a ddeml. Antes de que finalice, una aplicación debe llamar a **DdeFreeDataHandle** para liberar cualquier identificador de datos que haya creado pero que no se haya pasado a ddeml.

Una aplicación que aún no ha pasado el identificador a un objeto DDE a DDEML puede agregar datos al objeto o sobrescribir datos en el objeto mediante la función [**DdeAddData**](/windows/desktop/api/Ddeml/nf-ddeml-ddeadddata) . Normalmente, una aplicación utiliza **DdeAddData** para rellenar un objeto DDE no inicializado. Después de que una aplicación pase un identificador de datos a DDEML, no se puede cambiar el objeto DDE identificado por el identificador; solo se puede liberar.

 

 




