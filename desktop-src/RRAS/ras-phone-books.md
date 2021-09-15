---
title: Libros Teléfono RAS
description: Teléfono libros proporcionan una manera estándar de recopilar y especificar la información que el servicio de acceso Connection Manager para establecer una conexión remota.
ms.assetid: db6d076c-c683-4e27-ace1-d2c0cd0931f6
keywords:
- Teléfono libros, RAS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1bbdfe7d2293f87e01fe33f3a078f861a35a732d
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127476641"
---
# <a name="ras-phone-books"></a>Libros Teléfono RAS

Teléfono libros proporcionan una manera estándar de recopilar y especificar la información que el servicio de acceso Connection Manager para establecer una conexión remota. Teléfono libros asocian nombres de entrada con información como números de teléfono, puertos COM y configuración del módem. Cada entrada de la libreta de teléfonos contiene la información necesaria para establecer una conexión RAS.

Teléfono se almacenan en archivos de libros de teléfono, que son archivos de texto que contienen los nombres de entrada y la información asociada. RAS crea un archivo de libreta de teléfonos denominado RASPHONE. PBK. El usuario puede usar el cuadro de **Acceso telefónico a redes** principal para crear archivos de libreta de teléfono personales. La API ras no proporciona actualmente compatibilidad para crear un archivo de libreta de teléfonos. Algunas funciones RAS, como la [**función RasDial,**](/windows/desktop/api/Ras/nf-ras-rasdiala) tienen un parámetro que especifica un archivo de libreta de teléfonos. Si el autor de la llamada no especifica un archivo de libreta de teléfonos, la  función usa el archivo de libreta de teléfono predeterminado, que es el seleccionado por el usuario en la hoja de propiedades Preferencias del usuario del cuadro de diálogo **Acceso telefónico a redes** teléfono.

Windows NT 4.0 proporciona las funciones [**RasPhonebookDlg**](/windows/desktop/api/Rasdlg/nf-rasdlg-rasphonebookdlga) y [**RasEntryDlg**](/windows/desktop/api/Rasdlg/nf-rasdlg-rasentrydlga) que muestran la interfaz de usuario de RAS integrada que permite a los usuarios trabajar con las libretas de teléfonos y las entradas de las libretas de teléfonos.

**Windows 95:** Las redes de acceso telefónico almacenan las entradas de la libreta de teléfonos en el registro en lugar de en un archivo de libreta de teléfonos. Windows 95 no admite archivos de libreta de teléfonos ni funciones personales que muestren los cuadros de diálogo ras integrados.

 

 




