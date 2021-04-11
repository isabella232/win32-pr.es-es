---
title: Phone-Book entradas
description: Las entradas de libreta de teléfonos contienen la información necesaria para establecer una conexión RAS. Un usuario o administrador puede usar el cuadro de diálogo acceso telefónico a redes para crear, editar y marcar entradas de libreta de teléfonos.
ms.assetid: 971d7020-f9fd-42d1-97c3-79ad6eba6964
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 62cc01e66b5877c90b81610a5d8cf151b7cb7bd9
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104149520"
---
# <a name="phone-book-entries"></a>Phone-Book entradas

Las entradas de libreta de teléfonos contienen la información necesaria para establecer una conexión RAS. Un usuario o administrador puede usar el cuadro de diálogo **acceso telefónico a redes** para crear, editar y marcar entradas de libreta de teléfonos.

A partir de Windows NT Server 4,0, el sistema admite las funciones descritas para Windows 95, así como una serie de funciones adicionales que una aplicación puede usar para trabajar con las entradas de libretas de teléfonos y guías telefónicas.

La función [**RasEntryDlg**](/windows/desktop/api/Rasdlg/nf-rasdlg-rasentrydlga) muestra una hoja de propiedades que permite al usuario crear, editar o copiar entradas de libreta de teléfonos. Las funciones [**RasCreatePhonebookEntry**](/windows/desktop/api/Ras/nf-ras-rascreatephonebookentrya) y [**RasEditPhonebookEntry**](/windows/desktop/api/Ras/nf-ras-raseditphonebookentrya) llaman a la función **RasEntryDlg** . Puede usar la función [**RasRenameEntry**](/windows/desktop/api/Ras/nf-ras-rasrenameentrya) para cambiar el nombre de una entrada de libreta de teléfonos o [**RasDeleteEntry**](/windows/desktop/api/Ras/nf-ras-rasdeleteentrya) para eliminar una entrada. [**RasValidateEntryName**](/windows/desktop/api/Ras/nf-ras-rasvalidateentrynamea) determina si una cadena especificada tiene el formato correcto que se va a utilizar como nombre de entrada.

Puede usar [**RasGetEntryProperties**](/windows/desktop/api/Ras/nf-ras-rasgetentrypropertiesa) y [**RasSetEntryProperties**](/windows/desktop/api/Ras/nf-ras-rassetentrypropertiesa) para obtener y establecer información adicional sobre una entrada de libreta de teléfonos. Estas funciones usan una estructura [**RASENTRY**](/previous-versions/windows/desktop/legacy/aa377274(v=vs.85)) .

Las funciones [**RasGetCredentials**](/windows/desktop/api/Ras/nf-ras-rasgetcredentialsa) y [**RasSetCredentials**](/windows/desktop/api/Ras/nf-ras-rassetcredentialsa) obtienen y establecen las credenciales de usuario asociadas a una entrada de libreta de teléfonos ras especificada. Estas funciones usan una estructura [**RASCREDENTIALS**](/previous-versions/windows/desktop/legacy/aa376730(v=vs.85)) .

La función [**RasGetCountryInfo**](/windows/desktop/api/Ras/nf-ras-rasgetcountryinfoa) recupera información de marcado específica del país o la región de la lista de telefonía de Windows de los países. **RasGetCountryInfo** usa la estructura [**RASCTRYINFO**](/previous-versions/windows/desktop/legacy/aa376731(v=vs.85)) .

**Windows 95:  ** Admite un conjunto limitado de funciones para trabajar con entradas de libreta de teléfonos. Puede usar las funciones [**RasCreatePhonebookEntry**](/windows/desktop/api/Ras/nf-ras-rascreatephonebookentrya) y [**RasEditPhonebookEntry**](/windows/desktop/api/Ras/nf-ras-raseditphonebookentrya) para crear o editar una entrada de libreta de teléfonos. Estas funciones muestran un cuadro de diálogo en el que el usuario puede especificar información acerca de la entrada de la libreta de teléfonos. Puede usar las funciones [**RasGetEntryDialParams**](/windows/desktop/api/Ras/nf-ras-rasgetentrydialparamsa) y [**RasSetEntryDialParams**](/windows/desktop/api/Ras/nf-ras-rassetentrydialparamsa) para establecer o recuperar los parámetros de conexión para una entrada de libreta de teléfonos. La función [**RasEnumEntries**](/windows/desktop/api/Ras/nf-ras-rasenumentriesa) recupera una matriz de estructuras [**RASENTRYNAME**](/previous-versions/windows/desktop/legacy/aa377267(v=vs.85)) que contienen los nombres de las entradas del libro de teléfono.

 

 