---
description: En la ilustración siguiente se muestra la arquitectura general de los proveedores de servicios de telefonía y sus bibliotecas de vínculos dinámicos (dll de interfaz de usuario) asociadas.
ms.assetid: b5efe57a-19b8-49c5-810f-180633ed50d2
title: Arquitectura (API de telefonía)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 14423dba77af1ded38af4a6f2b896e76d28ca2cd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105687519"
---
# <a name="architecture-telephony-api"></a>Arquitectura (API de telefonía)

En la ilustración siguiente se muestra la arquitectura general de los proveedores de servicios de telefonía y sus bibliotecas de vínculos dinámicos (dll de interfaz de usuario) asociadas.

![profesionales y archivos dll de interfaz de usuario asociados](images/spuidl01.png)

El proveedor de servicios se compone de un mínimo de dos componentes. La DLL del proveedor de servicios (designada en la ilustración como MAIN). TSP) se ejecuta en el contexto del proceso TAPISRV y realiza todas las tareas del proveedor de servicios que no están relacionadas con los elementos de la interfaz de usuario asociados con el uso que hace una aplicación determinada del dispositivo (lo más probable es que, junto con los componentes de nivel inferior que no se muestran en la ilustración). Pero a diferencia de las versiones anteriores de TAPI en las que el código de la interfaz de usuario se integraba en el proveedor de servicios (y se ejecutaba, debido a la arquitectura anterior, en el contexto de la aplicación), el proveedor de servicios debe incluir ahora un componente independiente que implementa los elementos de la interfaz de usuario.

El archivo DLL de la interfaz de usuario del proveedor de servicios debe exportar las funciones a las que llama TAPI cuando la aplicación llama a funciones TAPI que generan la interfaz de usuario: [**TUISPI \_ lineConfigDialog**](/windows/win32/api/tspi/nf-tspi-tuispi_lineconfigdialog), [**TUISPI \_ lineConfigDialogEdit**](/windows/win32/api/tspi/nf-tspi-tuispi_lineconfigdialogedit), [**TUISPI \_ PhoneConfigDialog**](/windows/win32/api/tspi/nf-tspi-tuispi_phoneconfigdialog), [**TUISPI \_ providerConfig**](/windows/win32/api/tspi/nf-tspi-tuispi_providerconfig), [**TUISPI \_ providerInstall**](/windows/win32/api/tspi/nf-tspi-tuispi_providerinstall)y [**TUISPI \_ providerRemove**](/windows/win32/api/tspi/nf-tspi-tuispi_providerremove). Cada una de estas funciones incluye como parámetro un puntero a una función de devolución de llamada en TAPI, de tipo [**TUISPIDLLCALLBACK**](/windows/win32/api/tspi/nc-tspi-tuispidllcallback), que el archivo dll de la interfaz de usuario puede usar para comunicarse bidireccionalmente (tanto datos de envío como de recepción) con la dll del proveedor de servicios que se ejecuta en el proceso de TAPISRV. Si el proveedor de servicios genera una interfaz de usuario espontánea, como el cuadro de diálogo **Talk/colgar** de Unimodem, junto con cualquier función de TSPI para la que no se espera la interfaz de usuario (por ejemplo, cualquier función que no tenga un parámetro *hWnd* ), la dll de la interfaz de usuario debe exportar [**TUISPI \_ providerGenericDialog**](/windows/win32/api/tspi/nf-tspi-tuispi_providergenericdialog) y [**TUISPI \_ providerGenericDialogData**](/windows/win32/api/tspi/nf-tspi-tuispi_providergenericdialogdata).

> [!Note]  
> Las funciones de generación de interfaz de usuario de TSPI originales ( [**TSPI \_ lineConfigDialog**](/windows/win32/api/tspi/nf-tspi-tspi_lineconfigdialog), [**TSPI \_ lineConfigDialogEdit**](/windows/win32/api/tspi/nf-tspi-tspi_lineconfigdialogedit), [**TSPI \_ PhoneConfigDialog**](/windows/win32/api/tspi/nf-tspi-tspi_phoneconfigdialog), [**TSPI \_ providerConfig**](/windows/win32/api/tspi/nf-tspi-tspi_providerconfig), [**TSPI \_ providerInstall**](/windows/win32/api/tspi/nf-tspi-tspi_providerinstall)y [**TSPI \_ providerRemove**](/windows/win32/api/tspi/nf-tspi-tspi_providerremove)) están obsoletas y TAPI nunca lo llama. Por lo tanto, no es necesario que la DLL del proveedor de servicios exporte estos archivos. Sin embargo, si el proveedor de servicios desea aparecer como uno que se puede agregar mediante el panel de control de telefonía, una utilidad suministrada con telefonía de Windows en las versiones 1,4 y anteriores, debe exportar **TSPI \_ providerInstall**; si desea tener el botón [**quitar**](/windows/win32/api/tapi3if/nn-tapi3if-itcollection2) habilitado en el panel de control de telefonía cuando está seleccionado, debe exportar **TSPI \_ providerRemove** y, si desea que el botón de **instalación** esté habilitado en el panel de control de telefonía, debe exportar **TSPI \_ providerConfig**. El panel de control de telefonía comprueba la presencia de estas funciones en el archivo de proveedor de servicios TSP para ajustar su interfaz de usuario y reflejar las operaciones que se pueden realizar.

 

La DLL del proveedor de servicios debe exportar la función [**TSPI \_ providerUIIdentify**](/windows/win32/api/tspi/nf-tspi-tspi_provideruiidentify) que el proceso de TAPISRV utiliza para obtener el nombre del archivo dll de la interfaz de usuario que se va a cargar en el proceso de la aplicación. Debe exportar la función [**TSPI \_ providerGenericDialogData**](/windows/win32/api/tspi/nf-tspi-tspi_providergenericdialogdata) para recibir y responder a las solicitudes del archivo dll de la interfaz de usuario para que se muestren los datos, y debe exportar [**TSPI \_ providerFreeDialogInstance**](/windows/win32/api/tspi/nf-tspi-tspi_providerfreedialoginstance) for TAPISRV para indicar al proveedor de servicios Cuándo debe liberar una asociación establecida con el fin de generar la interfaz de usuario espontánea junto con una función que no está definida como presentación de la interfaz de usuario para el usuario. La DLL del proveedor de servicios puede enviar datos de forma unidireccional al archivo DLL de la interfaz de usuario mediante la nueva línea de mensaje TSPI [**\_ SENDDIALOGINSTANCEDATA**](line-senddialoginstancedata.md).

Dado que los nombres de las funciones TSPI y TUISPI se definen intencionadamente para ser diferentes, la DLL del proveedor de servicios y la DLL de la interfaz de usuario pueden ser el mismo archivo DLL, si se desea. Con la segmentación adecuada, esto no implica necesariamente el uso innecesario de memoria en el contexto de la aplicación y puede simplificar el proceso de instalación de los proveedores de servicios que se pueden implementar actualmente en un solo archivo DLL. TAPI solo llama a las funciones apropiadas para el contexto en el que se utiliza el archivo DLL.

El proveedor de servicios de telefonía y la DLL de la interfaz de usuario deben diseñarse con el requisito de que las funciones de la interfaz de usuario se pueden invocar desde varios procesos de la aplicación simultáneamente. También deben tener en cuenta que la aplicación y el servicio TAPI en el que se ejecuta el proveedor de servicios de telefonía pueden estar en equipos independientes de una LAN.

 

 
