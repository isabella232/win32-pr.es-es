---
description: Supongamos para los fines de un ejemplo que la aplicación llama a la función TAPI lineConfigDialog, que está diseñada para abrir un cuadro de diálogo para permitir la configuración de opciones del proveedor de servicios relacionadas con el dispositivo de línea especificado.
ms.assetid: a388d192-a327-4e67-968b-344d80c19fb1
title: Funciones diseñadas para generar la interfaz de usuario
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 63e7aeda54d4c04a144b2786b56f32d13c51ab39c5274204485151caecc2db1b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119140618"
---
# <a name="functions-designed-to-generate-ui"></a>Funciones diseñadas para generar la interfaz de usuario

Supongamos para los fines de un ejemplo que la aplicación llama a la función TAPI [**lineConfigDialog,**](/windows/win32/api/tapi/nf-tapi-lineconfigdialog) que está diseñada para abrir un cuadro de diálogo para permitir la configuración de opciones del proveedor de servicios relacionadas con el dispositivo de línea especificado. En respuesta a esta llamada, TAPI solicita a TAPISRV que llame a [**TSPI \_ providerUIIdentify**](/windows/win32/api/tspi/nf-tspi-tspi_provideruiidentify) en el proveedor de servicios de telefonía, obteniendo el nombre del archivo DLL de la interfaz de usuario de TSP.

En el contexto de la aplicación, TAPI carga el archivo DLL de la interfaz de usuario de TSP y llama a la función [**\_ lineConfigDialog de TUISPI**](/windows/win32/api/tspi/nf-tspi-tuispi_lineconfigdialog) con los parámetros proporcionados por la aplicación e incluye un puntero a la función TAPI [*DllCallbackProc.*](/windows/win32/api/tspi/nc-tspi-tuispidllcallback) El archivo DLL de la interfaz de usuario de TSP muestra el cuadro de diálogo de configuración, llamando a la función *DllCallbackProc* según sea necesario para obtener del proveedor de servicios de telefonía la información que se va a mostrar. Cada vez que se llama a la función *DllCallbackProc,* TAPI solicita a TAPISRV que llame a la función [**TSPI \_ providerGenericDialogData**](/windows/win32/api/tspi/nf-tspi-tspi_providergenericdialogdata) del proveedor de servicios de telefonía, pasando el bloque de parámetros desde el archivo DLL de la interfaz de usuario y devolviendo el bloque de parámetros al archivo DLL de la interfaz de usuario. El archivo DLL de la interfaz de usuario transmite los cambios de configuración al proveedor de servicios de telefonía mediante una *llamada a DllCallbackProc*.

Una vez completada la función, el archivo DLL de la interfaz de usuario devuelve de (en este caso) [**TUISPI \_ lineConfigDialog**](/windows/win32/api/tspi/nf-tspi-tuispi_lineconfigdialog). TAPI llama a la [**función FreeLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-freelibrary) para liberar el archivo DLL de la interfaz de usuario y vuelve a la aplicación.

 

 
