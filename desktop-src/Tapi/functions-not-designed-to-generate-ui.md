---
description: Suponga que el proveedor de servicios debe mostrar un cuadro de diálogo (como el cuadro de diálogo Unimodem o ATSP Talk/Hangup) durante el procesamiento de lineMakeCall o lineDial.
ms.assetid: 46f87947-bfcd-48ad-8c33-7ea4d9caa34c
title: Funciones no diseñadas para generar la interfaz de usuario
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a2a0cfb8168f4338ca5263abc067b141338caf1e24bef68c21241cfd6e53690d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120013215"
---
# <a name="functions-not-designed-to-generate-ui"></a>Funciones no diseñadas para generar la interfaz de usuario

Suponga que el proveedor de servicios debe mostrar un cuadro de diálogo (como el cuadro de diálogo Unimodem o ATSP **Talk/Hangup)** durante el procesamiento de [**lineMakeCall**](/windows/win32/api/tapi/nf-tapi-linemakecall) o [**lineDial**](/windows/win32/api/tapi/nf-tapi-linedial). En este caso, es el proveedor de servicios, no la aplicación, el que decide que se debe mostrar la interfaz de usuario.

Para invocar el archivo DLL de la interfaz de usuario en el proceso de aplicación, el proveedor de servicios llama a la devolución de llamada del evento de línea [*TSPI, \_*](/windows/win32/api/tspi/nc-tspi-lineevent) generando un mensaje [**LINE \_ CREATEDIALOGINSTANCE,**](line-createdialoginstance.md) pasando un puntero a una estructura de tipo [**TUISPICREATEDIALOGINSTANCEPARAMS**](/windows/win32/api/tspi/ns-tspi-tuispicreatedialoginstanceparams). Esta estructura contiene el **dwRequestID** de la función a la que está asociada la interfaz de usuario, lo que permite a TAPISRV identificar la aplicación cliente en la que se va a generar la interfaz de usuario.

TAPISRV solicita la instancia correcta de TAPI de la aplicación para cargar el archivo DLL de la interfaz de usuario y crear un subproceso para la interfaz de usuario dentro del proceso de la aplicación. Desde este nuevo subproceso de interfaz de usuario, TAPI llama a la función [**TUISPI \_ providerGenericDialog**](/windows/win32/api/tspi/nf-tspi-tuispi_providergenericdialog) del archivo DLL de la interfaz de usuario, pasando los datos especificados por el proveedor de servicios de telefonía en la estructura pasada con el mensaje [**LINE \_ CREATEDIALOGINSTANCE;**](line-createdialoginstance.md) el archivo DLL de la interfaz de usuario muestra el cuadro de diálogo adecuado (que es una cuestión de diseño privado entre la DLL de la interfaz de usuario y el proveedor de servicios de telefonía). El archivo DLL de la interfaz de usuario no devuelve del proveedor **de TUISPIGenericDialog \_** hasta que se cierra el cuadro de diálogo.

El proveedor de servicios de telefonía puede generar datos actualizados que se mostrarán en el cuadro de diálogo (o, por ejemplo, indicar al cuadro de diálogo que se cierre, si la llamada se abandona u se producen otros eventos) mediante el envío de un mensaje [**LINE \_ SENDDIALOGINSTANCEDATA.**](line-senddialoginstancedata.md) TAPISRV transmite los datos a TAPI, que llama a la función [**TUISPI \_ providerGenericDialogData**](/windows/win32/api/tspi/nf-tspi-tuispi_providergenericdialogdata) del archivo DLL de la interfaz de usuario. Este mecanismo proporciona un "envío" unidireccional al archivo DLL de la interfaz de usuario. Si el archivo DLL de la interfaz de usuario quiere informar al proveedor de servicios de telefonía de los resultados del cuadro de diálogo u obtener otros datos, puede llamar a la función [*DllCallbackProc*](/windows/win32/api/tspi/nc-tspi-tuispidllcallback) (un puntero al que recibió cuando se llamó al proveedor [**TUISPIGenericDialog). \_**](/windows/win32/api/tspi/nf-tspi-tuispi_providergenericdialog)

Cuando se descarta el cuadro de diálogo, [**el proveedor de TUISPIGenericDialog \_**](/windows/win32/api/tspi/nf-tspi-tuispi_providergenericdialog) vuelve a TAPI. TAPI llama [**a FreeLibrary para**](/windows/desktop/api/libloaderapi/nf-libloaderapi-freelibrary) liberar el archivo DLL de la interfaz de usuario y sale del subproceso de interfaz de usuario que había creado en el contexto de la aplicación. A continuación, solicita a TAPISRV que llame a la función [**TSPI \_ providerFreeDialogInstance**](/windows/win32/api/tspi/nf-tspi-tspi_providerfreedialoginstance) del proveedor de servicios de telefonía para desenlazar la asociación creada cuando el proveedor de servicios de telefonía envió originalmente el mensaje [**LINE \_ CREATEDIALOGINSTANCE.**](line-createdialoginstance.md) También se llama a esta función si el proceso de aplicación finaliza inesperadamente antes de que **tuISPI \_ providerGenericDialog devuelva.**

 

 
