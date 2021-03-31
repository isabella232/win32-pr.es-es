---
description: La interfaz ICertSrvSetup define los siguientes métodos. Los métodos de acceso de propiedad no se muestran aquí. Para ver las propiedades de ICertSrvSetup, consulte propiedades de ICertSrvSetup.
ms.assetid: cb7f288b-30a0-4c3b-b7bc-3055166d2302
title: Métodos de ICertSrvSetup
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3a4e3482de2c8c62db854b86d21e739993bc3bc8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103908085"
---
# <a name="methods-of-icertsrvsetup"></a>Métodos de ICertSrvSetup

La interfaz [**ICertSrvSetup**](/windows/desktop/api/Casetup/nn-casetup-icertsrvsetup) define los siguientes métodos. Los métodos de acceso de propiedad no se muestran aquí. Para ver las propiedades de **ICertSrvSetup**, consulte [propiedades de ICertSrvSetup](properties-of-icertsrvsetup.md).



| Método                                                                         | Descripción                                                                                                                                                                                                                                               |
|--------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CAImportPFX**](/windows/desktop/api/Casetup/nf-casetup-icertsrvsetup-caimportpfx)                               | Importa un certificado de entidad de certificación (CA) y su clave privada asociada en el almacén "LocalMachine".                                                                                                                                          |
| [**GetCASetupProperty**](/windows/desktop/api/Casetup/nf-casetup-icertsrvsetup-getcasetupproperty)                 | Obtiene un valor de propiedad para una configuración de CA.                                                                                                                                                                                                             |
| [**GetExistingCACertificates**](/windows/desktop/api/Casetup/nf-casetup-icertsrvsetup-getexistingcacertificates)   | Obtiene la colección de objetos **CCertSrvSetupKeyInformation** que representan los certificados de entidad de certificación válidos actualmente instalados en el equipo.                                                                                                                  |
| [**GetHashAlgorithmList**](/windows/desktop/api/Casetup/nf-casetup-icertsrvsetup-gethashalgorithmlist)             | Obtiene la lista de algoritmos hash admitidos por el [*proveedor de servicios criptográficos*](../secgloss/c-gly.md) (CSP) especificado para un algoritmo de firma de clave asimétrica. |
| [**GetKeyLengthList**](/windows/desktop/api/Casetup/nf-casetup-icertsrvsetup-getkeylengthlist)                     | Obtiene la lista de longitudes de clave admitidas por el CSP especificado.                                                                                                                                                                                              |
| [**GetPrivateKeyContainerList**](/windows/desktop/api/Casetup/nf-casetup-icertsrvsetup-getprivatekeycontainerlist) | Obtiene la lista de nombres de contenedores de claves almacenados por el CSP especificado para los algoritmos de clave de firma asimétrica.                                                                                                                                                 |
| [**GetProviderNameList**](/windows/desktop/api/Casetup/nf-casetup-icertsrvsetup-getprovidernamelist)               | Obtiene la lista de CSP que proporcionan algoritmos de firma de clave asimétrica en el equipo.                                                                                                                                                                   |
| [**GetSupportedCATypes**](/windows/desktop/api/Casetup/nf-casetup-icertsrvsetup-getsupportedcatypes)               | Obtiene los tipos de CA que se pueden instalar en un equipo bajo el contexto del autor de la llamada.                                                                                                                                                                       |
| [**InitializeDefaults**](/windows/desktop/api/Casetup/nf-casetup-icertsrvsetup-initializedefaults)                 | Inicializa un objeto **CCertSrvSetup** con los valores predeterminados para habilitar la instalación de un rol de CA.                                                                                                                                                           |
| [**Instalar**](/windows/desktop/api/Casetup/nf-casetup-icertsrvsetup-install)                                       | Instala un rol de CA como configurado en el objeto **CCertSrvSetup** .                                                                                                                                                                                         |
| [**IsPropertyEditable**](/windows/desktop/api/Casetup/nf-casetup-icertsrvsetup-ispropertyeditable)                 | Indica al llamador si se puede editar una propiedad especificada.                                                                                                                                                                                       |
| [**PostUnInstall**](/windows/desktop/api/Casetup/nf-casetup-icertsrvsetup-postuninstall)                           | No está implementado y está reservado para uso futuro.                                                                                                                                                                                                        |
| [**PreUnInstall**](/windows/desktop/api/Casetup/nf-casetup-icertsrvsetup-preuninstall)                             | Guarda temporalmente la información de estado específica de los roles.                                                                                                                                                                                                        |
| [**SetCADistinguishedName**](/windows/desktop/api/Casetup/nf-casetup-icertsrvsetup-setcadistinguishedname)         | Establece un nombre común de CA y un sufijo de nombre distintivo opcional.                                                                                                                                                                                          |
| [**SetCASetupProperty**](/windows/desktop/api/Casetup/nf-casetup-icertsrvsetup-setcasetupproperty)                 | Establece un valor de propiedad para una configuración de CA.                                                                                                                                                                                                             |
| [**SetDatabaseInformation**](/windows/desktop/api/Casetup/nf-casetup-icertsrvsetup-setdatabaseinformation)         | Establece la información relacionada con la base de datos para el rol de CA.                                                                                                                                                                                                    |
| [**SetParentCAInformation**](/windows/desktop/api/Casetup/nf-casetup-icertsrvsetup-setparentcainformation)         | Establece la información de CA primaria para una configuración de CA subordinada.                                                                                                                                                                                        |
| [**SetWebCAInformation**](/windows/desktop/api/Casetup/nf-casetup-icertsrvsetup-setwebcainformation)               | Establece la información de la entidad de certificación para el rol inscripción Web de CA.                                                                                                                                                                                                   |



 

 

 
