---
description: Métodos definidos por la interfaz IMSCEPSetup.
ms.assetid: 0d41243f-cff1-4608-bbe6-f99dc548b0e2
title: Métodos de IMSCEPSetup
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6f543bb4525a3335128846ec5724e1a9a09a35f7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104542334"
---
# <a name="methods-of-imscepsetup"></a>Métodos de IMSCEPSetup

La interfaz [**IMSCEPSetup**](/windows/desktop/api/Casetup/nn-casetup-imscepsetup) define los siguientes métodos. Los métodos de acceso de propiedad no se muestran aquí. Para ver las propiedades de **IMSCEPSetup**, consulte [propiedades de IMSCEPSetup](properties-of-imscepsetup.md).



| Método                                                             | Descripción                                                                                                                                                                                                                                                                       |
|--------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**GetKeyLengthList**](/windows/desktop/api/Casetup/nf-casetup-imscepsetup-getkeylengthlist)           | Obtiene la lista de [*longitudes de clave*](../secgloss/k-gly.md) admitidas por el [*proveedor de servicios criptográficos*](../secgloss/c-gly.md) (CSP) especificado. |
| [**GetMSCEPSetupProperty**](/windows/desktop/api/Casetup/nf-casetup-imscepsetup-getmscepsetupproperty) | Obtiene un valor de propiedad para una configuración del servicio de inscripción de dispositivos de red (NDES).                                                                                                                                                                                               |
| [**GetProviderNameList**](/windows/desktop/api/Casetup/nf-casetup-imscepsetup-getprovidernamelist)     | Obtiene la lista de CSP que proporcionan la firma de clave asimétrica y los algoritmos de intercambio en el equipo.                                                                                                                                                                              |
| [**InitializeDefaults**](/windows/desktop/api/Casetup/nf-casetup-imscepsetup-initializedefaults)       | Inicializa un objeto **CMSCEPSetup** con los valores predeterminados para habilitar la instalación de un rol ndes.                                                                                                                                                                                  |
| [**Instalar**](/windows/desktop/api/Casetup/nf-casetup-imscepsetup-install)                             | Instala un rol tal como está configurado en el objeto **CMSCEPSetup** .                                                                                                                                                                                                                      |
| [**IsMSCEPStoreEmpty**](/windows/desktop/api/Casetup/nf-casetup-imscepsetup-ismscepstoreempty)         | Siempre devuelve **Variant \_ true** y no debe usarse.                                                                                                                                                                                                                          |
| [**PostUnInstall**](/windows/desktop/api/Casetup/nf-casetup-imscepsetup-postuninstall)                 | Este método no se implementa. Queda reservada para uso futuro.                                                                                                                                                                                                                    |
| [**PreUnInstall**](/windows/desktop/api/Casetup/nf-casetup-imscepsetup-preuninstall)                   | Quita la configuración del registro y de IIS para el rol NDES.                                                                                                                                                                                                                              |
| [**SetAccountInformation**](/windows/desktop/api/Casetup/nf-casetup-imscepsetup-setaccountinformation) | Establece la información de la cuenta de usuario utilizada por la extensión NDES de IIS para realizar la inscripción en nombre de los dispositivos de red.                                                                                                                                                              |
| [**SetMSCEPSetupProperty**](/windows/desktop/api/Casetup/nf-casetup-imscepsetup-setmscepsetupproperty) | Establece un valor de propiedad para una configuración de NDES.                                                                                                                                                                                                                                  |



 

 

 
