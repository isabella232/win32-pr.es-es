---
description: Los archivos de configuración de identidad y grupo del mismo nivel se pueden importar y exportar de un punto de conexión a otro mediante las funciones de importación y exportación de identidades ubicadas en las API de Identity Manager y agrupación.
ms.assetid: 876d9c57-15f6-4f5e-8035-792e15f8035e
title: Importación y exportación de la configuración de identidad y grupo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a356f2747e3c8276446568b6f82bcbd773b14af8
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127069239"
---
# <a name="identity-and-group-configuration-import-and-export"></a>Importación y exportación de la configuración de identidad y grupo

Los archivos de configuración de identidad y grupo del mismo nivel se pueden importar y exportar de un punto de conexión a otro mediante las funciones de importación y exportación de identidades ubicadas en las API de Identity Manager y agrupación. Estas funciones son útiles porque permiten a un usuario exportar de forma rápida y cómoda identidades y agrupar información de configuración de un equipo a otro.

## <a name="importing-and-exporting-peer-identity-data"></a>Importación y exportación de datos de identidad del mismo nivel

Los datos de identidad de un elemento del mismo nivel se exportan mediante una llamada a [**PeerIdentityExport**](/windows/desktop/api/P2P/nf-p2p-peeridentityexport) con el nombre de identidad que se va a exportar y una contraseña usada para cifrar las credenciales asociadas. Esta función devuelve una cadena XML que contiene el nombre de identidad del elemento del mismo nivel y las credenciales cifradas para esa identidad específica, que luego se pueden pasar a un equipo diferente mediante un mecanismo de transferencia externo, como el correo electrónico. En el ejemplo siguiente se muestra el formato de la cadena XML:

``` syntax
<PEERIDENTITYEXPORT VERSION="1.0">
   <PEERNAME>
     <!-- UTF-8 encoded peer name of the identity -->
   </PEERNAME>
   <DATA xmlns:dt="urn:schemas-microsoft-com:datatypes" dt:dt="bin.base64">
      <!-- base64 encoded / PFX encoded and encrypted IDC with the private key -->
   </DATA>
</PEERIDENTITYEXPORT>
```

Los datos de identidad exportados se pueden recuperar llamando a [**PeerIdentityImport**](/windows/desktop/api/P2P/nf-p2p-peeridentityimport)y pasando la cadena XML con la contraseña proporcionada en la llamada anterior a [**PeerIdentityExport**](/windows/desktop/api/P2P/nf-p2p-peeridentityexport). Esta función devuelve el nombre del mismo nivel de la identidad importada. El nombre y las credenciales de identidad importados se pueden usar igual que un nombre de identidad devuelto por [**PeerEnumIdentities**](/windows/desktop/api/P2P/nf-p2p-peerenumidentities) o [**PeerIdentityCreate**](/windows/desktop/api/P2P/nf-p2p-peeridentitycreate).

> [!Note]  
> Al llamar [**a PeerIdentityExport,**](/windows/desktop/api/P2P/nf-p2p-peeridentityexport)el usuario de la aplicación o la API debe proporcionar una contraseña segura de longitud suficiente. Esto es importante porque los datos de identidad importados contienen la clave privada de la identidad.

 

## <a name="importing-and-exporting-a-group-identity-configuration"></a>Importar y exportar una configuración de identidad de grupo

La agrupación del mismo nivel permite que un elemento del mismo nivel exporte datos de configuración de grupo de un punto de conexión a otro mediante API de importación y exportación específicas. Para importar datos de configuración, la identidad del elemento del mismo nivel que realiza la importación (y quién realizó anteriormente la exportación) debe estar presente en el equipo donde se importarán los datos de configuración. Esta identidad se puede obtener exportando e importando mediante los métodos especificados en la sección anterior de este tema: Importar y exportar datos de [identidad del mismo nivel](#importing-and-exporting-peer-identity-data).

Los datos de configuración de grupo contienen toda la información para que una identidad se una a un grupo desde un nuevo punto de conexión. En concreto, los datos de configuración contienen la cadena GMC, el nombre del mismo nivel de grupo, el nombre de la nube, el ámbito y un conjunto de marcas específicas de PNRP. Para una identidad propietaria de un grupo, se incluye una clave privada para el grupo en la información de configuración del grupo.

> [!Note]  
> Al llamar [**a PeerGroupExportConfig,**](/windows/desktop/api/P2P/nf-p2p-peergroupexportconfig)un usuario de aplicación o API debe proporcionar una contraseña segura de longitud suficiente. Esto es importante porque los datos de identidad importados contienen la clave privada del grupo.

 

Para exportar la configuración actual del grupo del mismo nivel, llame a [**PeerGroupExportConfig**](/windows/desktop/api/P2P/nf-p2p-peergroupexportconfig), pasando el identificador al grupo (obtenido por una llamada anterior a [**PeerGroupJoin,**](/windows/desktop/api/P2P/nf-p2p-peergroupjoin) [**PeerGroupOpen**](/windows/desktop/api/P2P/nf-p2p-peergroupopen)o [**PeerGroupCreate)**](/windows/desktop/api/P2P/nf-p2p-peergroupcreate)y una contraseña usada para cifrar y proteger el archivo de configuración. Esta función devuelve una cadena XML que contiene la configuración en el formato del ejemplo siguiente, que se puede escribir en un archivo y pasar a otro equipo mediante un mecanismo de transferencia externo, como correo electrónico.

``` syntax
<PEERGROUPCONFIG VERSION="1.0">
  <IDENTITYPEERNAME>
    <!-- UTF-8 encoded peer name of the identity -->
  </IDENTITYPEERNAME>
  <GROUPPEERNAME>
    <!-- UTF-8 encoded peer name of the group -->
  </GROUPPEERNAME>
  <CLOUDNAME>
    <!-- UTF-8 encoded Unicode name of the cloud -->
  </CLOUDNAME>
  <SCOPE>
    <!-- UTF-8 encoded Unicode name of the scope: global, site-local, link-local -->
  </SCOPE>
  <CLOUDFLAGS>
    <!-- A DWORD that contains cloud-specific settings, represented as a string -->
  </CLOUDFLAGS>
  <GMC xmlns:dt="urn:schemas-microsoft-com:datatypes" dt:dt="bin.base64">
    <!-- base64/PKCS7 encoded GMC chain -->
  </GMC>
</PEERGROUPCONFIG>
```

Después de obtener la configuración del grupo como una cadena XML, el grupo se puede importar llamando a [**PeerGroupImportConfig**](/windows/desktop/api/P2P/nf-p2p-peergroupimportconfig) con la cadena XML de configuración y la contraseña específica proporcionada a [**PeerGroupExportConfig.**](/windows/desktop/api/P2P/nf-p2p-peergroupexportconfig) Esta función devuelve un nombre de identidad y un nombre de grupo del mismo nivel, que se pueden proporcionar a [**PeerGroupOpen**](/windows/desktop/api/P2P/nf-p2p-peergroupopen) y una conexión al grupo establecido.

 

 



