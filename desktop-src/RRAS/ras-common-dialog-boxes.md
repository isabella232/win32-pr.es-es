---
title: Cuadros de diálogo comunes de RAS
description: Windows proporciona un conjunto de funciones que muestran los cuadros de diálogo de RAS proporcionados por el sistema.
ms.assetid: 8231511a-7339-4fbb-8a39-f643ac575856
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3032da8b0647b48941d85fc4f085ddb8ced0125f
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104149570"
---
# <a name="ras-common-dialog-boxes"></a>Cuadros de diálogo comunes de RAS

Windows proporciona un conjunto de funciones que muestran los cuadros de diálogo de RAS proporcionados por el sistema. Estas funciones facilitan a las aplicaciones mostrar una interfaz de usuario conocida para que los usuarios puedan realizar tareas de RAS. Por ejemplo, los usuarios pueden establecer y supervisar las conexiones o trabajar con entradas de libreta de teléfonos. Windows 95 no admite actualmente estas funciones.

La función [**RasPhonebookDlg**](/windows/desktop/api/Rasdlg/nf-rasdlg-rasphonebookdlga) muestra el cuadro de diálogo principal **redes de acceso telefónico** . Desde este cuadro de diálogo, el usuario puede marcar, editar o eliminar una entrada de libreta de teléfonos seleccionada, crear una nueva entrada de libreta de teléfonos o especificar preferencias del usuario. La función **RasPhonebookDlg** utiliza la estructura [**RASPBDLG**](/previous-versions/windows/desktop/legacy/aa377607(v=vs.85)) para especificar parámetros de entrada y salida adicionales. Por ejemplo, puede establecer miembros de la estructura para controlar la posición del cuadro de diálogo en la pantalla. Puede usar la estructura **RASPBDLG** para especificar una función de devolución de llamada [**RasPBDlgFunc**](/windows/desktop/api/Rasdlg/nc-rasdlg-raspbdlgfunca) que recibe notificaciones de la actividad del usuario mientras el cuadro de diálogo está abierto. Por ejemplo, RAS llama a la función **RasPBDlgFunc** si el usuario marca, edita, crea o elimina una entrada de libreta de teléfonos.

Puede usar la función [**RasDialDlg**](/windows/desktop/api/Rasdlg/nf-rasdlg-rasdialdlga) para iniciar una operación de conexión RAS sin mostrar el cuadro de diálogo principal **redes de acceso telefónico** . Con **RasDialDlg**, debe especificar un número de teléfono o una entrada de libreta de teléfonos a la que llamar. La función muestra un flujo de cuadros de diálogo que indican el estado de la operación de conexión. La función **RasDialDlg** usa una estructura [**RasDialDlg**](/previous-versions/windows/desktop/legacy/aa377023(v=vs.85)) para especificar parámetros de entrada y salida adicionales, como la posición del cuadro de diálogo y la subentrada de la libreta de teléfonos a la que se va a llamar.

Para mostrar la hoja de propiedades **acceso telefónico a redes** , llame a la función [**RasMonitorDlg**](/previous-versions/windows/desktop/legacy/aa377584(v=vs.85)) . Este cuadro de diálogo permite al usuario supervisar el estado de las conexiones existentes. La función **RasMonitorDlg** usa una estructura [**RasMonitorDlg**](/previous-versions/windows/desktop/legacy/aa377591(v=vs.85)) para especificar parámetros de entrada y salida adicionales, como la posición del cuadro de diálogo y la página de la hoja de propiedades que se va a mostrar en la parte superior.

Puede llamar a la función [**RasEntryDlg**](/windows/desktop/api/Rasdlg/nf-rasdlg-rasentrydlga) para mostrar una hoja de propiedades para crear, editar o copiar una entrada de libreta de teléfonos. La función **RasEntryDlg** usa una estructura [**RasEntryDlg**](/previous-versions/windows/desktop/legacy/aa377260(v=vs.85)) para especificar parámetros de entrada y salida adicionales, como la posición del cuadro de diálogo y el tipo de operación de libreta de teléfonos.

 

 