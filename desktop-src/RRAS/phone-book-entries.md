---
title: Phone-Book entradas
description: Teléfono entradas del libro contienen la información necesaria para establecer una conexión RAS. Un usuario o administrador puede usar el cuadro Acceso telefónico a redes diálogo para crear, editar y marcar entradas de la libreta de teléfonos.
ms.assetid: 971d7020-f9fd-42d1-97c3-79ad6eba6964
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ea62595504229dd5dd920385a92214156a7d112774cb3fefbaff3f1b5edc7cbe
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117789825"
---
# <a name="phone-book-entries"></a>Phone-Book entradas

Teléfono entradas del libro contienen la información necesaria para establecer una conexión RAS. Un usuario o administrador puede usar el **cuadro Acceso telefónico a redes** diálogo para crear, editar y marcar entradas de la libreta de teléfonos.

A partir de Windows NT Server 4.0, el sistema admite las funciones descritas para Windows 95, así como una serie de funciones adicionales que una aplicación puede usar para trabajar con las libretas telefónicas y las entradas de la libreta de teléfonos.

La [**función RasEntryDlg**](/windows/desktop/api/Rasdlg/nf-rasdlg-rasentrydlga) muestra una hoja de propiedades que permite al usuario crear, editar o copiar entradas de la libreta de teléfonos. Las [**funciones RasCreatePhonebookEntry**](/windows/desktop/api/Ras/nf-ras-rascreatephonebookentrya) y [**RasEditPhonebookEntry**](/windows/desktop/api/Ras/nf-ras-raseditphonebookentrya) llaman a **la función RasEntryDlg.** Puede usar la función [**RasRenameEntry para**](/windows/desktop/api/Ras/nf-ras-rasrenameentrya) cambiar el nombre de una entrada de la libreta de teléfonos o [**RasDeleteEntry para**](/windows/desktop/api/Ras/nf-ras-rasdeleteentrya) eliminar una entrada. [**RasValidateEntryName**](/windows/desktop/api/Ras/nf-ras-rasvalidateentrynamea) determina si una cadena especificada tiene el formato correcto para usarse como nombre de entrada.

Puede usar [**RasGetEntryProperties**](/windows/desktop/api/Ras/nf-ras-rasgetentrypropertiesa) y [**RasSetEntryProperties**](/windows/desktop/api/Ras/nf-ras-rassetentrypropertiesa) para obtener y establecer información adicional sobre una entrada de guía telefónica. Estas funciones usan una [**estructura RASENTRY.**](/previous-versions/windows/desktop/legacy/aa377274(v=vs.85))

Las [**funciones RasGetCredentials**](/windows/desktop/api/Ras/nf-ras-rasgetcredentialsa) y [**RasSetCredentials**](/windows/desktop/api/Ras/nf-ras-rassetcredentialsa) obtienen y establecen las credenciales de usuario asociadas a una entrada de la libreta de teléfono RAS especificada. Estas funciones usan una [**estructura RASCREDENTIALS.**](/previous-versions/windows/desktop/legacy/aa376730(v=vs.85))

La [**función RasGetCountryInfo**](/windows/desktop/api/Ras/nf-ras-rasgetcountryinfoa) recupera información de marcado específica del país o región de la Windows de países. **RasGetCountryInfo** usa la [**estructura RASCTRYINFO.**](/previous-versions/windows/desktop/legacy/aa376731(v=vs.85))

**Windows 95: ** Admite un conjunto limitado de funciones para trabajar con entradas de la libreta de teléfonos. Puede usar las funciones [**RasCreatePhonebookEntry**](/windows/desktop/api/Ras/nf-ras-rascreatephonebookentrya) y [**RasEditPhonebookEntry**](/windows/desktop/api/Ras/nf-ras-raseditphonebookentrya) para crear o editar una entrada de libro de teléfono. Estas funciones muestran un cuadro de diálogo en el que el usuario puede especificar información sobre la entrada de la libreta de teléfonos. Puede usar las [**funciones RasGetEntryDialParams**](/windows/desktop/api/Ras/nf-ras-rasgetentrydialparamsa) y [**RasSetEntryDialParams**](/windows/desktop/api/Ras/nf-ras-rassetentrydialparamsa) para establecer o recuperar los parámetros de conexión de una entrada de la libreta de teléfonos. La [**función RasEnumEntries**](/windows/desktop/api/Ras/nf-ras-rasenumentriesa) recupera una matriz de estructuras [**RASENTRYNAME**](/previous-versions/windows/desktop/legacy/aa377267(v=vs.85)) que contienen los nombres de entrada de la libreta de teléfonos.

 

 