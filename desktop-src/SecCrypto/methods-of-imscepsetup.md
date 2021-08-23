---
description: Métodos definidos por la interfaz IMSCEPSetup.
ms.assetid: 0d41243f-cff1-4608-bbe6-f99dc548b0e2
title: Métodos de IMSCEPSetup
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2d7dcadeb6c3815a37f1b1e87453a7ff737c70f53d76e0904bc67211ed7028f2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119622235"
---
# <a name="methods-of-imscepsetup"></a>Métodos de IMSCEPSetup

La interfaz [**IMSCEPSetup**](/windows/desktop/api/Casetup/nn-casetup-imscepsetup) define los métodos siguientes. Los métodos de acceso de propiedad no se muestran aquí. Para ver las propiedades de **IMSCEPSetup,** vea [Propiedades de IMSCEPSetup](properties-of-imscepsetup.md).



| Método                                                             | Descripción                                                                                                                                                                                                                                                                       |
|--------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**GetKeyLengthList**](/windows/desktop/api/Casetup/nf-casetup-imscepsetup-getkeylengthlist)           | Obtiene la lista de [*longitudes de clave admitidas*](../secgloss/k-gly.md) por el proveedor de [*servicios criptográficos (CSP) especificado.*](../secgloss/c-gly.md) |
| [**GetMSCEPSetupProperty**](/windows/desktop/api/Casetup/nf-casetup-imscepsetup-getmscepsetupproperty) | Obtiene un valor de propiedad para una Servicio de inscripción de dispositivos de red (NDES).                                                                                                                                                                                               |
| [**GetProviderNameList**](/windows/desktop/api/Casetup/nf-casetup-imscepsetup-getprovidernamelist)     | Obtiene la lista de CSP que proporcionan algoritmos de intercambio y firma de clave asimétrica en el equipo.                                                                                                                                                                              |
| [**InitializeDefaults**](/windows/desktop/api/Casetup/nf-casetup-imscepsetup-initializedefaults)       | Inicializa un objeto **CMSCEPSetup con** valores predeterminados para habilitar la instalación de un rol NDES.                                                                                                                                                                                  |
| [**Instalar**](/windows/desktop/api/Casetup/nf-casetup-imscepsetup-install)                             | Instala un rol tal como está configurado en el **objeto CMSCEPSetup.**                                                                                                                                                                                                                      |
| [**IsMSCEPStoreEmpty**](/windows/desktop/api/Casetup/nf-casetup-imscepsetup-ismscepstoreempty)         | Siempre devuelve **VARIANT \_ TRUE y** no se debe usar.                                                                                                                                                                                                                          |
| [**PostUnInstall**](/windows/desktop/api/Casetup/nf-casetup-imscepsetup-postuninstall)                 | Este método no se implementa. Queda reservada para uso futuro.                                                                                                                                                                                                                    |
| [**PreUnInstall**](/windows/desktop/api/Casetup/nf-casetup-imscepsetup-preuninstall)                   | Quita la configuración del Registro e IIS para el rol NDES.                                                                                                                                                                                                                              |
| [**SetAccountInformation**](/windows/desktop/api/Casetup/nf-casetup-imscepsetup-setaccountinformation) | Establece la información de la cuenta de usuario utilizada por la extensión NDES de IIS para realizar la inscripción en nombre de los dispositivos de red.                                                                                                                                                              |
| [**SetMSCEPSetupProperty**](/windows/desktop/api/Casetup/nf-casetup-imscepsetup-setmscepsetupproperty) | Establece un valor de propiedad para una configuración de NDES.                                                                                                                                                                                                                                  |



 

 

 
