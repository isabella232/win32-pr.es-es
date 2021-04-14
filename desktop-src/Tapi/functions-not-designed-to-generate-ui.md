---
description: Supongamos que el proveedor de servicios debe mostrar un cuadro de diálogo (por ejemplo, el cuadro de diálogo de hablar/colgar de Unimodem o ATSP) durante el procesamiento de lineMakeCall o lineal.
ms.assetid: 46f87947-bfcd-48ad-8c33-7ea4d9caa34c
title: Funciones no diseñadas para generar la interfaz de usuario
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 70bd7ed1395136d1a2d2a31b060127395e8804ac
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104545446"
---
# <a name="functions-not-designed-to-generate-ui"></a>Funciones no diseñadas para generar la interfaz de usuario

Supongamos que el proveedor de servicios debe mostrar un cuadro de diálogo (por ejemplo, el cuadro de diálogo de **hablar/colgar** de Unimodem o ATSP) durante el procesamiento de [**lineMakeCall**](/windows/win32/api/tapi/nf-tapi-linemakecall) o [**lineal**](/windows/win32/api/tapi/nf-tapi-linedial). En este caso, es el proveedor de servicios, no la aplicación, que decide que se debe mostrar la interfaz de usuario.

Para invocar el archivo DLL de la interfaz de usuario en el proceso de la aplicación, el proveedor de servicios llama a la devolución de llamada de [*\_ evento de línea*](/windows/win32/api/tspi/nc-tspi-lineevent) de TSPI, generando un mensaje de [**línea \_ CREATEDIALOGINSTANCE**](line-createdialoginstance.md) , pasando un puntero a una estructura de tipo [**TUISPICREATEDIALOGINSTANCEPARAMS**](/windows/win32/api/tspi/ns-tspi-tuispicreatedialoginstanceparams). Esta estructura contiene el **dwRequestID** de la función a la que está asociada la interfaz de usuario, lo que permite a TAPISRV identificar la aplicación cliente en la que se va a generar la interfaz de usuario.

TAPISRV solicita la instancia de la aplicación correcta de TAPI para cargar el archivo DLL de la interfaz de usuario y crear un subproceso para la interfaz de usuario en el proceso de la aplicación. Desde este nuevo subproceso de la interfaz de usuario, TAPI llama a la función [**\_ providerGenericDialog**](/windows/win32/api/tspi/nf-tspi-tuispi_providergenericdialog) de la dll TUISPI de la interfaz de usuario, pasando los datos especificados por el proveedor de servicios de telefonía en la estructura pasada con el mensaje de la [**línea \_ CREATEDIALOGINSTANCE**](line-createdialoginstance.md) ; el archivo dll de la interfaz de usuario muestra el cuadro de diálogo correspondiente (que es una cuestión para el diseño privado entre el archivo dll de la La DLL de la interfaz de usuario no devuelve de **TUISPI \_ providerGenericDialog** hasta que se cierre el cuadro de diálogo.

El proveedor de servicios de telefonía puede generar datos actualizados para que se muestren en el cuadro de diálogo (o, por ejemplo, indicar al cuadro de diálogo que se cierre, si se abandona la llamada o se producen otros eventos) mediante el envío de un mensaje de [**\_ SENDDIALOGINSTANCEDATA de línea**](line-senddialoginstancedata.md) . TAPISRV transmite los datos a TAPI, que llama a la función [**TUISPI \_ providerGenericDialogData**](/windows/win32/api/tspi/nf-tspi-tuispi_providergenericdialogdata) de la dll de la interfaz de usuario. Este mecanismo proporciona un "envío" unidireccional al archivo DLL de la interfaz de usuario. Si el archivo DLL de la interfaz de usuario desea informar al proveedor de servicios de telefonía de los resultados del cuadro de diálogo u obtener otros datos, puede llamar a la función [*DllCallbackProc*](/windows/win32/api/tspi/nc-tspi-tuispidllcallback) (un puntero al que recibió cuando se llamó a [**TUISPI \_ providerGenericDialog**](/windows/win32/api/tspi/nf-tspi-tuispi_providergenericdialog) ).

Cuando se descarta el cuadro de diálogo, [**TUISPI \_ providerGenericDialog**](/windows/win32/api/tspi/nf-tspi-tuispi_providergenericdialog) vuelve a TAPI. TAPI llama a [**FreeLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-freelibrary) para liberar el archivo dll de la interfaz de usuario y sale del subproceso de interfaz de usuario que se creó en el contexto de la aplicación. A continuación, solicita a TAPISRV que llame a la función [**TSPI \_ providerFreeDialogInstance**](/windows/win32/api/tspi/nf-tspi-tspi_providerfreedialoginstance) del proveedor de servicios de telefonía para desenlazar la asociación creada cuando el proveedor de servicios de telefonía envió originalmente el mensaje de [**línea \_ CREATEDIALOGINSTANCE**](line-createdialoginstance.md) . También se llama a esta función si el proceso de la aplicación finaliza de forma inesperada antes de que **TUISPI \_ providerGenericDialog** devuelva.

 

 
