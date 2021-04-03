---
title: Libretas de teléfonos RAS
description: Las libretas de teléfonos proporcionan una manera estándar de recopilar y especificar la información que el administrador de conexiones de acceso remoto necesita para establecer una conexión remota.
ms.assetid: db6d076c-c683-4e27-ace1-d2c0cd0931f6
keywords:
- Libretas de teléfonos, RAS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1bbdfe7d2293f87e01fe33f3a078f861a35a732d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104075821"
---
# <a name="ras-phone-books"></a>Libretas de teléfonos RAS

Las libretas de teléfonos proporcionan una manera estándar de recopilar y especificar la información que el administrador de conexiones de acceso remoto necesita para establecer una conexión remota. Las libretas de teléfonos asocian nombres de entradas a información como números de teléfono, puertos COM y configuraciones de módem. Cada entrada de libreta de teléfonos contiene la información necesaria para establecer una conexión RAS.

Las libretas de teléfonos se almacenan en archivos de libreta de teléfonos, que son archivos de texto que contienen los nombres de entrada y la información asociada. RAS crea un archivo de libreta de teléfonos denominado RASPHONE. PBK. El usuario puede usar el cuadro de diálogo principal **redes de acceso telefónico** para crear archivos de libreta de teléfonos personales. La API de RAS no es compatible actualmente con la creación de un archivo de libreta de teléfonos. Algunas funciones RAS, como la función [**rasdial**](/windows/desktop/api/Ras/nf-ras-rasdiala) , tienen un parámetro que especifica un archivo de libreta de teléfonos. Si el autor de la llamada no especifica un archivo de libreta de teléfonos, la función utiliza el archivo de libreta de teléfonos predeterminado, que es el seleccionado por el usuario en la hoja de propiedades **preferencias del usuario** del cuadro de diálogo **acceso telefónico a redes** .

Windows NT 4,0 proporciona las funciones [**RasPhonebookDlg**](/windows/desktop/api/Rasdlg/nf-rasdlg-rasphonebookdlga) y [**RasEntryDlg**](/windows/desktop/api/Rasdlg/nf-rasdlg-rasentrydlga) que muestran la interfaz de usuario ras integrada que permite a los usuarios trabajar con las libretas de teléfonos y entradas de libreta de teléfonos.

**Windows 95:** Acceso telefónico a redes almacena entradas de libreta de teléfonos en el registro en lugar de en un archivo de libreta de teléfonos. Windows 95 no admite archivos de libreta de teléfonos personales ni funciones que muestren los cuadros de diálogo de RAS integrados.

 

 




