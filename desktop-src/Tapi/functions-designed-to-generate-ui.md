---
description: Supongamos, por ejemplo, que la aplicación llama a la función lineConfigDialog de TAPI, que está diseñada para abrir un cuadro de diálogo con el fin de permitir la configuración de las opciones del proveedor de servicios relacionadas con el dispositivo de línea especificado.
ms.assetid: a388d192-a327-4e67-968b-344d80c19fb1
title: Funciones diseñadas para generar la interfaz de usuario
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fa360effd2a1504d2325be2131c430664f1e7a5c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104001155"
---
# <a name="functions-designed-to-generate-ui"></a>Funciones diseñadas para generar la interfaz de usuario

Supongamos, por ejemplo, que la aplicación llama a la función [**lineConfigDialog**](/windows/win32/api/tapi/nf-tapi-lineconfigdialog) de TAPI, que está diseñada para abrir un cuadro de diálogo con el fin de permitir la configuración de las opciones del proveedor de servicios relacionadas con el dispositivo de línea especificado. En respuesta a esta llamada, TAPI solicita a TAPISRV que llame a [**TSPI \_ providerUIIdentify**](/windows/win32/api/tspi/nf-tspi-tspi_provideruiidentify) en el proveedor de servicios de telefonía, obteniendo el nombre del archivo dll de la interfaz de usuario de TSP.

En el contexto de la aplicación, TAPI carga el archivo DLL de la interfaz de usuario de TSP y llama a la función [**\_ LineConfigDialog de TUISPI**](/windows/win32/api/tspi/nf-tspi-tuispi_lineconfigdialog) con los parámetros proporcionados por la aplicación, e incluye un puntero a la función [*DllCallbackProc*](/windows/win32/api/tspi/nc-tspi-tuispidllcallback) de TAPI. El archivo DLL de la interfaz de usuario de TSP muestra el cuadro de diálogo Configuración, que llama a la función *DllCallbackProc* según sea necesario para obtener del proveedor de servicios de telefonía la información que se va a mostrar. Cada vez que se llama a la función *DllCallbackProc* , TAPI solicita TAPISRV para llamar a la función [**\_ providerGenericDialogData de TSPI**](/windows/win32/api/tspi/nf-tspi-tspi_providergenericdialogdata) del proveedor de servicios de telefonía, pasando el bloque de parámetros del archivo dll de la interfaz de usuario y devolviendo el bloque de parámetros al archivo dll de la interfaz de usuario. El archivo DLL de la interfaz de usuario transmite cualquier cambio de configuración al proveedor de servicios de telefonía llamando a *DllCallbackProc*.

Una vez completada la función, la DLL de la interfaz de usuario vuelve de (en este caso) [**TUISPI \_ lineConfigDialog**](/windows/win32/api/tspi/nf-tspi-tuispi_lineconfigdialog). TAPI llama a la función [**FreeLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-freelibrary) para liberar el archivo dll de la interfaz de usuario y vuelve a la aplicación.

 

 
