---
description: La interfaz ICertSrvSetup define los métodos siguientes. Los métodos de acceso de propiedad no se muestran aquí. Para ver las propiedades de ICertSrvSetup, consulte Propiedades de ICertSrvSetup.
ms.assetid: cb7f288b-30a0-4c3b-b7bc-3055166d2302
title: Métodos de ICertSrvSetup
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 28274e1f59a4c229587f7e9f73222381ca89cff1a112ef7dc633f7a0c32dd434
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119407895"
---
# <a name="methods-of-icertsrvsetup"></a>Métodos de ICertSrvSetup

La interfaz [**ICertSrvSetup**](/windows/desktop/api/Casetup/nn-casetup-icertsrvsetup) define los métodos siguientes. Los métodos de acceso de propiedad no se muestran aquí. Para ver las propiedades de **ICertSrvSetup,** vea [Propiedades de ICertSrvSetup.](properties-of-icertsrvsetup.md)



| Método                                                                         | Descripción                                                                                                                                                                                                                                               |
|--------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CAImportPFX**](/windows/desktop/api/Casetup/nf-casetup-icertsrvsetup-caimportpfx)                               | Importa un certificado de entidad de certificación (CA) y su clave privada asociada en el almacén "LocalMachine".                                                                                                                                          |
| [**GetCASetupProperty**](/windows/desktop/api/Casetup/nf-casetup-icertsrvsetup-getcasetupproperty)                 | Obtiene un valor de propiedad para una configuración de CA.                                                                                                                                                                                                             |
| [**GetExistingCACertificates**](/windows/desktop/api/Casetup/nf-casetup-icertsrvsetup-getexistingcacertificates)   | Obtiene la colección de **objetos CCertSrvSetupKeyInformation** que representan certificados de entidad de certificación válidos instalados actualmente en el equipo.                                                                                                                  |
| [**GetHashAlgorithmList**](/windows/desktop/api/Casetup/nf-casetup-icertsrvsetup-gethashalgorithmlist)             | Obtiene la lista de algoritmos hash admitidos por el proveedor de [*servicios criptográficos*](../secgloss/c-gly.md) (CSP) especificado para un algoritmo de firma de clave asimétrica. |
| [**GetKeyLengthList**](/windows/desktop/api/Casetup/nf-casetup-icertsrvsetup-getkeylengthlist)                     | Obtiene la lista de longitudes de clave admitidas por el CSP especificado.                                                                                                                                                                                              |
| [**GetPrivateKeyContainerList**](/windows/desktop/api/Casetup/nf-casetup-icertsrvsetup-getprivatekeycontainerlist) | Obtiene la lista de nombres de contenedor de claves almacenados por el CSP especificado para algoritmos de clave de firma asimétrica.                                                                                                                                                 |
| [**GetProviderNameList**](/windows/desktop/api/Casetup/nf-casetup-icertsrvsetup-getprovidernamelist)               | Obtiene la lista de CSP que proporcionan algoritmos de firma de clave asimétrica en el equipo.                                                                                                                                                                   |
| [**GetSupportedCATypes**](/windows/desktop/api/Casetup/nf-casetup-icertsrvsetup-getsupportedcatypes)               | Obtiene los tipos de CA que se pueden instalar en un equipo en el contexto del autor de la llamada.                                                                                                                                                                       |
| [**InitializeDefaults**](/windows/desktop/api/Casetup/nf-casetup-icertsrvsetup-initializedefaults)                 | Inicializa un objeto **CCertSrvSetup con** valores predeterminados para habilitar la instalación de un rol de ca.                                                                                                                                                           |
| [**Instalar**](/windows/desktop/api/Casetup/nf-casetup-icertsrvsetup-install)                                       | Instala un rol de ca tal como está configurado en el **objeto CCertSrvSetup.**                                                                                                                                                                                         |
| [**IsPropertyEditable**](/windows/desktop/api/Casetup/nf-casetup-icertsrvsetup-ispropertyeditable)                 | Indica al autor de la llamada si se puede editar una propiedad especificada.                                                                                                                                                                                       |
| [**PostUnInstall**](/windows/desktop/api/Casetup/nf-casetup-icertsrvsetup-postuninstall)                           | No se implementa y está reservado para su uso futuro.                                                                                                                                                                                                        |
| [**PreUnInstall**](/windows/desktop/api/Casetup/nf-casetup-icertsrvsetup-preuninstall)                             | Guarda temporalmente información de estado específica del rol.                                                                                                                                                                                                        |
| [**SetCADistinguishedName**](/windows/desktop/api/Casetup/nf-casetup-icertsrvsetup-setcadistinguishedname)         | Establece un nombre común de entidad de certificación y un sufijo de nombre distintivo opcional.                                                                                                                                                                                          |
| [**SetCASetupProperty**](/windows/desktop/api/Casetup/nf-casetup-icertsrvsetup-setcasetupproperty)                 | Establece un valor de propiedad para una configuración de ca.                                                                                                                                                                                                             |
| [**SetDatabaseInformation**](/windows/desktop/api/Casetup/nf-casetup-icertsrvsetup-setdatabaseinformation)         | Establece la información relacionada con la base de datos para el rol de ca.                                                                                                                                                                                                    |
| [**SetParentCAInformation**](/windows/desktop/api/Casetup/nf-casetup-icertsrvsetup-setparentcainformation)         | Establece la información de ca primaria para una configuración de CA subordinada.                                                                                                                                                                                        |
| [**SetWebCAInformation**](/windows/desktop/api/Casetup/nf-casetup-icertsrvsetup-setwebcainformation)               | Establece la información de ca para el rol de inscripción web de ca.                                                                                                                                                                                                   |



 

 

 
