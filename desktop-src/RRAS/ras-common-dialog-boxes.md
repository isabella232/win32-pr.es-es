---
title: Cuadros de diálogo comunes de RAS
description: Windows proporciona un conjunto de funciones que muestran los cuadros de diálogo RAS proporcionados por el sistema.
ms.assetid: 8231511a-7339-4fbb-8a39-f643ac575856
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5be93db8e8d1819abe56d98bb293a7b6b027089be0648b00f7848d5204e911ff
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119909725"
---
# <a name="ras-common-dialog-boxes"></a>Cuadros de diálogo comunes de RAS

Windows proporciona un conjunto de funciones que muestran los cuadros de diálogo RAS proporcionados por el sistema. Estas funciones permiten a las aplicaciones mostrar fácilmente una interfaz de usuario conocida para que los usuarios puedan realizar tareas RAS. Por ejemplo, los usuarios pueden establecer y supervisar las conexiones, o trabajar con entradas de la libreta de teléfonos. Windows 95 no admite actualmente estas funciones.

La [**función RasPhonebookDlg**](/windows/desktop/api/Rasdlg/nf-rasdlg-rasphonebookdlga) muestra el cuadro de **diálogo Acceso telefónico a redes** principal. En este cuadro de diálogo, el usuario puede marcar, editar o eliminar una entrada seleccionada de la libreta de teléfonos, crear una nueva entrada de libro de teléfono o especificar las preferencias del usuario. La **función RasPhonebookDlg** usa la [**estructura RASPBDLG**](/previous-versions/windows/desktop/legacy/aa377607(v=vs.85)) para especificar parámetros de entrada y salida adicionales. Por ejemplo, puede establecer miembros de la estructura para controlar la posición del cuadro de diálogo en la pantalla. Puede usar la **estructura RASPBDLG** para especificar una función de devolución de llamada [**RasPBDlgFunc**](/windows/desktop/api/Rasdlg/nc-rasdlg-raspbdlgfunca) que recibe notificaciones de actividad del usuario mientras el cuadro de diálogo está abierto. Por ejemplo, RAS llama a la función **RasPBDlgFunc** si el usuario marca, edita, crea o elimina una entrada de la libreta de teléfonos.

Puede usar la función [**RasDialDlg**](/windows/desktop/api/Rasdlg/nf-rasdlg-rasdialdlga) para iniciar una operación de conexión RAS sin mostrar el cuadro de **Acceso telefónico a redes** principal. Con **RasDialDlg,** especifique un número de teléfono o una entrada de la libreta de teléfonos a la que llamar. La función muestra una secuencia de cuadros de diálogo que indican el estado de la operación de conexión. La **función RasDialDlg** usa una estructura [**RASDIALDLG**](/previous-versions/windows/desktop/legacy/aa377023(v=vs.85)) para especificar parámetros de entrada y salida adicionales, como la posición del cuadro de diálogo y la subentrada de la libreta de teléfonos a la que se llamará.

Para mostrar la **Acceso telefónico a redes** de propiedades, llame a la [**función RasMonitorDlg.**](/previous-versions/windows/desktop/legacy/aa377584(v=vs.85)) Este cuadro de diálogo permite al usuario supervisar el estado de las conexiones existentes. La **función RasMonitorDlg** usa una estructura [**RASMONITORDLG**](/previous-versions/windows/desktop/legacy/aa377591(v=vs.85)) para especificar parámetros de entrada y salida adicionales, como la posición del cuadro de diálogo y la página de la hoja de propiedades que se mostrará en la parte superior.

Puede llamar a la [**función RasEntryDlg**](/windows/desktop/api/Rasdlg/nf-rasdlg-rasentrydlga) para mostrar una hoja de propiedades para crear, editar o copiar una entrada de la libreta de teléfonos. La **función RasEntryDlg** usa una estructura [**RASENTRYDLG**](/previous-versions/windows/desktop/legacy/aa377260(v=vs.85)) para especificar parámetros de entrada y salida adicionales, como la posición del cuadro de diálogo y el tipo de operación de la libreta de teléfonos.

 

 