---
description: En la ilustración siguiente se muestra la arquitectura general de los proveedores de servicios de telefonía y sus bibliotecas de vínculos dinámicos de interfaz de usuario (DLL de interfaz de usuario) asociadas.
ms.assetid: b5efe57a-19b8-49c5-810f-180633ed50d2
title: Arquitectura (API de telefonía)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 96d37c2911a664fee2670a41444ee01e4390c8ee5dd526bf550b75eab4990009
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118871988"
---
# <a name="architecture-telephony-api"></a>Arquitectura (API de telefonía)

En la ilustración siguiente se muestra la arquitectura general de los proveedores de servicios de telefonía y sus bibliotecas de vínculos dinámicos de interfaz de usuario (DLL de interfaz de usuario) asociadas.

![tsps y archivos DLL de interfaz de usuario asociados](images/spuidl01.png)

El proveedor de servicios consta de un mínimo de dos componentes. Dll del proveedor de servicios (designada en la ilustración como MAIN). TSP) se ejecuta en el contexto del proceso TAPISRV y realiza todas las tareas del proveedor de servicios que no están relacionadas con los elementos de la interfaz de usuario asociados con el uso del dispositivo por parte de una aplicación determinada (lo más probable es que junto con los componentes de nivel inferior no se muestran en la ilustración). Pero a diferencia de las versiones anteriores de TAPI en las que el código de la interfaz de usuario se integraba en el proveedor de servicios (y se ejecutaba, debido a la arquitectura anterior, en el contexto de la aplicación), el proveedor de servicios ahora debe incluir un componente independiente que implemente los elementos de la interfaz de usuario.

El archivo DLL de interfaz de usuario del proveedor de servicios debe exportar las funciones a las que llama TAPI cuando la aplicación llama a funciones TAPI que generan la interfaz de usuario: [**TUISPI \_ lineConfigDialog,**](/windows/win32/api/tspi/nf-tspi-tuispi_lineconfigdialog) [**TUISPI \_ lineConfigDialogEdit,**](/windows/win32/api/tspi/nf-tspi-tuispi_lineconfigdialogedit) [**TUISPI \_ phoneConfigDialog,**](/windows/win32/api/tspi/nf-tspi-tuispi_phoneconfigdialog) [**TUISPI \_ providerConfig,**](/windows/win32/api/tspi/nf-tspi-tuispi_providerconfig) [**TUISPI \_ providerInstall**](/windows/win32/api/tspi/nf-tspi-tuispi_providerinstall)y [**TUISPI \_ providerRemove**](/windows/win32/api/tspi/nf-tspi-tuispi_providerremove). Cada una de estas funciones incluye como parámetro un puntero a una función de devolución de llamada en TAPI, de tipo [**TUISPIDLLCALLBACK**](/windows/win32/api/tspi/nc-tspi-tuispidllcallback), que el archivo DLL de interfaz de usuario puede usar para comunicarse bidireccionalmente (enviar y recibir datos) con el archivo DLL del proveedor de servicios que se ejecuta en el proceso TAPISRV. Si el proveedor de servicios genera alguna vez una interfaz de usuario esparádico, como el cuadro de diálogo Unimodem **Talk/Hangup,** junto con cualquier función TSPI para la que no se espera la interfaz de usuario (por ejemplo, cualquier función que no tenga un parámetro *hwnd),* el archivo DLL de la interfaz de usuario debe exportar [**tuispi \_ providerGenericDialog**](/windows/win32/api/tspi/nf-tspi-tuispi_providergenericdialog) y [**tuispi \_ providerGenericDialogData**](/windows/win32/api/tspi/nf-tspi-tuispi_providergenericdialogdata).

> [!Note]  
> Las funciones originales que generan la interfaz de usuario de [**TSPI (TSPI \_ lineConfigDialog**](/windows/win32/api/tspi/nf-tspi-tspi_lineconfigdialog), [**TSPI \_ lineConfigDialogEdit,**](/windows/win32/api/tspi/nf-tspi-tspi_lineconfigdialogedit) [**TSPI \_ phoneConfigDialog,**](/windows/win32/api/tspi/nf-tspi-tspi_phoneconfigdialog) [**TSPI \_ providerConfig,**](/windows/win32/api/tspi/nf-tspi-tspi_providerconfig) [**TSPI \_ providerInstall**](/windows/win32/api/tspi/nf-tspi-tspi_providerinstall)y [**TSPI \_ providerRemove)**](/windows/win32/api/tspi/nf-tspi-tspi_providerremove)están obsoletas y tapI nunca las llama. Por lo tanto, no es necesario que el archivo DLL del proveedor de servicios los exporte. Sin embargo, si el proveedor de servicios desea aparecer como uno que se puede agregar mediante el proveedor de telefonía Panel de control, una utilidad suministrada con la telefonía Windows en las [](/windows/win32/api/tapi3if/nn-tapi3if-itcollection2) versiones 1.4 y anteriores, debe exportar **proveedor de TSPIInstalar \_**;  si quiere que el botón Quitar esté habilitado en el Panel de control de telefonía cuando esté seleccionada, debe exportar proveedor **de \_ TSPIRemove;** y si quiere que el botón Configurar esté habilitado en el Panel de control de telefonía cuando esté seleccionado, debe exportar **proveedor \_ TSPIConfig**. El proveedor de Panel de control comprueba la presencia de estas funciones en el archivo TSP del proveedor de servicios para ajustar su interfaz de usuario para reflejar qué operaciones se pueden realizar.

 

El archivo DLL del proveedor de servicios debe exportar la función [**TSPI \_ providerUIIdentify**](/windows/win32/api/tspi/nf-tspi-tspi_provideruiidentify) que el proceso TAPISRV usa para obtener el nombre del archivo DLL de interfaz de usuario que se cargará en el proceso de aplicación. Debe exportar la función [**\_ providerGenericDialogData**](/windows/win32/api/tspi/nf-tspi-tspi_providergenericdialogdata) de TSPI para recibir y responder a las solicitudes del archivo DLL de interfaz de usuario para que se muestren los datos, y debe exportar el proveedor [**de \_ TSPIFreeDialogInstance**](/windows/win32/api/tspi/nf-tspi-tspi_providerfreedialoginstance) para el proceso TAPISRV para que le diga al proveedor de servicios cuándo liberar una asociación establecida con el fin de generar una interfaz de usuario estival junto con una función que no está definida como presentación de la interfaz de usuario al usuario. El archivo DLL del proveedor de servicios puede enviar datos unidireccionalmente al archivo DLL de interfaz de usuario mediante el nuevo mensaje de TSPI [**LINE \_ SENDDIALOGINSTANCEDATA**](line-senddialoginstancedata.md).

Dado que los nombres de las funciones TSPI y TUISPI se definen intencionadamente para ser diferentes, el archivo DLL del proveedor de servicios y el archivo DLL de interfaz de usuario pueden ser el mismo archivo DLL, si lo desea. Con una segmentación adecuada, esto no da lugar necesariamente a un uso innecesario de memoria en el contexto de la aplicación y puede simplificar el proceso de instalación de los proveedores de servicios que se pueden implementar actualmente en un único archivo DLL. TAPI llama solo a las funciones adecuadas para el contexto en el que se usa el archivo DLL.

Tanto el proveedor de servicios de telefonía como el archivo DLL de interfaz de usuario deben diseñarse con el requisito de que las funciones de interfaz de usuario se puedan invocar desde varios procesos de aplicación simultáneamente. También deben tener en cuenta que la aplicación y el servicio TAPI bajo el que se ejecuta el proveedor de servicios de telefonía pueden estar en equipos independientes en una LAN.

 

 
