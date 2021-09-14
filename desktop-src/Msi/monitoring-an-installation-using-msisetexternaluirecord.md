---
description: Los autores de paquetes pueden supervisar los mensajes internos de Windows Installer mediante la creación de una aplicación ejecutable que contiene un controlador de devolución de llamada basado en registros para recibir los mensajes y la funcionalidad para iniciar una instalación.
ms.assetid: 5d9e51dd-7918-491f-aea9-01a6e0317c57
title: Supervisión de una instalación mediante MsiSetExternalUIRecord
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ce3fd0caf3d24eed49ff8a373b6f4d38037f840f
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127261100"
---
# <a name="monitoring-an-installation-using-msisetexternaluirecord"></a>Supervisión de una instalación mediante MsiSetExternalUIRecord

Los autores de paquetes pueden supervisar los mensajes internos de Windows Installer mediante la creación de una aplicación ejecutable que contiene un controlador de devolución de llamada basado en registros para recibir los mensajes y la funcionalidad para iniciar una instalación.

El controlador basado en registros del ejemplo siguiente se ajusta al prototipo [**INSTALLUI \_ HANDLER \_ RECORD**](/windows/win32/api/msi/nc-msi-installui_handler_record) y se pasa un puntero a este controlador de devolución de llamada a la función [**MsiSetExternalUIRecord.**](/windows/desktop/api/Msi/nf-msi-msisetexternaluirecord)


```C++
//
// ExternalUIRecord.cpp : Defines the entry point for the console application.
//
#include <tchar.h>
#include <windows.h>
#include <stdio.h>
#include <msi.h>
#include <msiquery.h>
#pragma comment(lib, "msi.lib")
#pragma comment(lib, "user32.lib")
#ifndef _WIN32_MSI
#define _WIN32_MSI    310
#endif 

void Usage(LPCTSTR szProgram)
{
_tprintf(TEXT("Usage: %s <path to .MSI package>\n"), szProgram);
return;
}

// In the following snippet, the hRecord parameter is used only
// to format the displayed message. However, because hRecord is 
// a handle to a MSI record, the MSI API could be called to
// obtain information. The external UI handler should not close
// hRecord because the handle belongs to the Windows Installer.

INT CALLBACK UIHandler(LPVOID pvContext, UINT uiMessageType, MSIHANDLE hRecord)
{
INSTALLMESSAGE iMessage = (INSTALLMESSAGE)(0xFF000000 & uiMessageType);
BOOL bMessage = (INSTALLMESSAGE_ERROR == iMessage);
BOOL bFatalExit = (INSTALLMESSAGE_FATALEXIT == iMessage);
BOOL bWarning = (INSTALLMESSAGE_WARNING == iMessage);

if ((bMessage || bFatalExit || bWarning) && hRecord && pvContext)
{
TCHAR rgchMessage[1024];
DWORD dwMessage = sizeof(rgchMessage)/sizeof(TCHAR);
LPTSTR pszMessage = rgchMessage;

UINT uiRet = MsiFormatRecord(*(MSIHANDLE*)pvContext, 
                                 hRecord, pszMessage, &dwMessage);
if (ERROR_MORE_DATA == uiRet)
{
// Allocate a buffer to hold the string and terminating null.
pszMessage = new TCHAR[++dwMessage];
if (!pszMessage)
{
// no memory, return an error
return -1;
}
uiRet = MsiFormatRecord(*(MSIHANDLE*)pvContext, 
                                 hRecord, pszMessage, &dwMessage);
if (ERROR_SUCCESS != uiRet)
{
// Return an error if an unexpected error occurs.
if (rgchMessage != pszMessage)
    delete [] pszMessage;
return -1;
}
}
TCHAR rgchFatalError[] = TEXT("Fatal Error");
TCHAR rgchError[] = TEXT("Error");
TCHAR rgchWarning[] = TEXT("Warning");
TCHAR* pszCaption = NULL;

if (INSTALLMESSAGE_ERROR == iMessage)
    pszCaption = rgchError;
else if (INSTALLMESSAGE_FATALEXIT == iMessage)
    pszCaption = rgchFatalError;
else if (INSTALLMESSAGE_WARNING == iMessage)
    pszCaption = rgchWarning;

int iResponse = MessageBox(NULL, pszMessage, 
                         pszCaption, uiMessageType & 0x00FFFFFF);

if (rgchMessage != pszMessage)
    delete [] pszMessage;
return iResponse;
}

// Signal that the handler handled this message.
return IDOK;
}

// A console application that takes the path to a package,
// installs the package silently, and uses a record based 
// external UI handler to display any error.

int _tmain(int argc, _TCHAR* argv[])
{
UINT uiRet = ERROR_SUCCESS;
MSIHANDLE hProduct = NULL;

if (2 != argc)
{
    // Incorrect command line used.
    Usage(argv[0]);
    uiRet = 1;
    goto End;
}

// Because thid example won't restore the UI level,
// ignore return value.
MsiSetInternalUI(INSTALLUILEVEL_NONE, /* pWnd */ NULL);

uiRet = MsiOpenPackage(argv[1], &hProduct);
if (ERROR_SUCCESS != uiRet)
{
    _tprintf(TEXT("ERROR: Failed to open %s database.\n"), argv[1]);
    uiRet = 1;
    goto End;
}

// set the external UI handler
DWORD dwMessageFilter = INSTALLLOGMODE_FATALEXIT
       | INSTALLLOGMODE_ERROR | INSTALLLOGMODE_WARNING;

//Pass the pointer to hProduct as the pvContext argument, 
// so that the record based external UI handler
// can use it to format the records we send to it.

uiRet = MsiSetExternalUIRecord(UIHandler, 
              dwMessageFilter, (LPVOID)&hProduct, /* ppuiPrevHandle */ NULL);

if (ERROR_SUCCESS != uiRet)
{
    _tprintf(TEXT("ERROR: Failed to set the external UI handler.\n"));
    uiRet = 1;
    goto End;
}

// Do the default action and install the product.
uiRet = MsiDoAction(hProduct, TEXT(""));

End:
// Close opened resources.
if (hProduct)
    MsiCloseHandle(hProduct);

return ERROR_SUCCESS == uiRet ? 0 : 1;
}
//
```



 

 
