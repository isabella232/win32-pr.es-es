---
description: Los archivos de configuración de grupo y de identidad del mismo nivel se pueden importar y exportar de un punto de conexión a otro mediante las funciones de importación y exportación de identidades que se encuentran en Identity Manager y las API de agrupación.
ms.assetid: 876d9c57-15f6-4f5e-8035-792e15f8035e
title: Importación y exportación de configuración de identidad y grupo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a356f2747e3c8276446568b6f82bcbd773b14af8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103813827"
---
# <a name="identity-and-group-configuration-import-and-export"></a><span data-ttu-id="df7b5-103">Importación y exportación de configuración de identidad y grupo</span><span class="sxs-lookup"><span data-stu-id="df7b5-103">Identity and Group Configuration Import and Export</span></span>

<span data-ttu-id="df7b5-104">Los archivos de configuración de grupo y de identidad del mismo nivel se pueden importar y exportar de un punto de conexión a otro mediante las funciones de importación y exportación de identidades que se encuentran en Identity Manager y las API de agrupación.</span><span class="sxs-lookup"><span data-stu-id="df7b5-104">Peer identity and group configuration files can be imported and exported from one endpoint to another by using the identity import and export functions located in the Identity Manager and Grouping APIs.</span></span> <span data-ttu-id="df7b5-105">Estas funciones son útiles porque permiten que un usuario exporte de forma rápida y cómoda las identidades y la información de configuración de un equipo a otro equipo.</span><span class="sxs-lookup"><span data-stu-id="df7b5-105">These functions are useful because they allow a user to quickly and conveniently export identities and group configuration information from one computer to another computer.</span></span>

## <a name="importing-and-exporting-peer-identity-data"></a><span data-ttu-id="df7b5-106">Importar y exportar datos de identidad del mismo nivel</span><span class="sxs-lookup"><span data-stu-id="df7b5-106">Importing and Exporting Peer Identity Data</span></span>

<span data-ttu-id="df7b5-107">Los datos de identidad de un elemento del mismo nivel se exportan llamando a [**PeerIdentityExport**](/windows/desktop/api/P2P/nf-p2p-peeridentityexport) con el nombre de identidad que se va a exportar y una contraseña usada para cifrar las credenciales asociadas.</span><span class="sxs-lookup"><span data-stu-id="df7b5-107">The identity data of a peer is exported by calling [**PeerIdentityExport**](/windows/desktop/api/P2P/nf-p2p-peeridentityexport) with the identity name to export and a password used to encrypt the associated credentials.</span></span> <span data-ttu-id="df7b5-108">Esta función devuelve una cadena XML que contiene el nombre de identidad del elemento del mismo nivel y las credenciales cifradas para esa identidad específica, que se pueden pasar a un equipo diferente mediante un mecanismo de transferencia externo, como el correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="df7b5-108">This function returns an XML string that contains the identity name of the peer and the encrypted credentials for that specific identity, which can then be passed to a different computer by using an external transfer mechanism, such as e-mail.</span></span> <span data-ttu-id="df7b5-109">En el ejemplo siguiente se muestra el formato de la cadena XML:</span><span class="sxs-lookup"><span data-stu-id="df7b5-109">The following example shows you the format of the XML string:</span></span>

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

<span data-ttu-id="df7b5-110">Los datos de identidad exportados se pueden recuperar llamando a [**PeerIdentityImport**](/windows/desktop/api/P2P/nf-p2p-peeridentityimport)y pasando la cadena XML con la contraseña proporcionada en la llamada anterior a [**PeerIdentityExport**](/windows/desktop/api/P2P/nf-p2p-peeridentityexport).</span><span class="sxs-lookup"><span data-stu-id="df7b5-110">The exported identity data can be retrieved by calling [**PeerIdentityImport**](/windows/desktop/api/P2P/nf-p2p-peeridentityimport), and passing in the XML string with the password supplied in the previous call to [**PeerIdentityExport**](/windows/desktop/api/P2P/nf-p2p-peeridentityexport).</span></span> <span data-ttu-id="df7b5-111">Esta función devuelve el nombre del mismo nivel de la identidad importada.</span><span class="sxs-lookup"><span data-stu-id="df7b5-111">This function returns the peer name of the imported identity.</span></span> <span data-ttu-id="df7b5-112">El nombre de identidad y las credenciales importados se pueden usar como un nombre de identidad devuelto por [**PeerEnumIdentities**](/windows/desktop/api/P2P/nf-p2p-peerenumidentities) o [**PeerIdentityCreate**](/windows/desktop/api/P2P/nf-p2p-peeridentitycreate).</span><span class="sxs-lookup"><span data-stu-id="df7b5-112">The imported identity name and credentials can be used just like an identity name returned by [**PeerEnumIdentities**](/windows/desktop/api/P2P/nf-p2p-peerenumidentities) or [**PeerIdentityCreate**](/windows/desktop/api/P2P/nf-p2p-peeridentitycreate).</span></span>

> [!Note]  
> <span data-ttu-id="df7b5-113">Al llamar a [**PeerIdentityExport**](/windows/desktop/api/P2P/nf-p2p-peeridentityexport), el usuario de la aplicación o de la API debe proporcionar una contraseña segura de longitud suficiente.</span><span class="sxs-lookup"><span data-stu-id="df7b5-113">When calling [**PeerIdentityExport**](/windows/desktop/api/P2P/nf-p2p-peeridentityexport), the application or API user must provide a strong password of sufficient length.</span></span> <span data-ttu-id="df7b5-114">Esto es importante porque los datos de identidad importados contienen la clave privada de la identidad.</span><span class="sxs-lookup"><span data-stu-id="df7b5-114">This is important because the imported identity data contains the private key for the identity.</span></span>

 

## <a name="importing-and-exporting-a-group-identity-configuration"></a><span data-ttu-id="df7b5-115">Importación y exportación de una configuración de identidad de grupo</span><span class="sxs-lookup"><span data-stu-id="df7b5-115">Importing and Exporting a Group Identity Configuration</span></span>

<span data-ttu-id="df7b5-116">La agrupación del mismo nivel permite a un elemento del mismo nivel exportar datos de configuración de grupo de un punto de conexión a otro usando API de importación y exportación específicas.</span><span class="sxs-lookup"><span data-stu-id="df7b5-116">Peer Grouping allows a peer to export group configuration data from one endpoint to another by using specific import and export APIs.</span></span> <span data-ttu-id="df7b5-117">Para importar los datos de configuración, la identidad del elemento del mismo nivel que realiza la importación (y quién realizó previamente la exportación) debe estar presente en el equipo en el que se van a importar los datos de configuración.</span><span class="sxs-lookup"><span data-stu-id="df7b5-117">To import configuration data, the identity of the peer performing the import (and who previously performed the export) must be present on the computer where the configuration data is to be imported.</span></span> <span data-ttu-id="df7b5-118">Esta identidad se puede obtener exportándolos e importándola mediante los métodos especificados en la sección anterior de este tema: [importar y exportar datos de identidad del mismo nivel](#importing-and-exporting-peer-identity-data).</span><span class="sxs-lookup"><span data-stu-id="df7b5-118">This identity can be obtained by exporting and importing it by the methods specified in the previous section of this topic: [Importing and Exporting Peer Identity Data](#importing-and-exporting-peer-identity-data).</span></span>

<span data-ttu-id="df7b5-119">Los datos de configuración del grupo contienen toda la información de una identidad para unirse a un grupo desde un nuevo punto de conexión.</span><span class="sxs-lookup"><span data-stu-id="df7b5-119">The group configuration data contains all of the information for an identity to join a group from a new endpoint.</span></span> <span data-ttu-id="df7b5-120">En concreto, los datos de configuración contienen la cadena GMC, el nombre del mismo nivel del grupo, el nombre de la nube, el ámbito y un conjunto de marcas específicas PNRP.</span><span class="sxs-lookup"><span data-stu-id="df7b5-120">Specifically, the configuration data contains the GMC chain, group peer name, cloud name, scope, and a set of PNRP specific flags.</span></span> <span data-ttu-id="df7b5-121">En el caso de una identidad que posee un grupo, se incluye una clave privada para el grupo en la información de configuración del grupo.</span><span class="sxs-lookup"><span data-stu-id="df7b5-121">For an identity that owns a group, a private key for the group is included in the group configuration information.</span></span>

> [!Note]  
> <span data-ttu-id="df7b5-122">Al llamar a [**PeerGroupExportConfig**](/windows/desktop/api/P2P/nf-p2p-peergroupexportconfig), una aplicación o un usuario de la API debe proporcionar una contraseña segura de longitud suficiente.</span><span class="sxs-lookup"><span data-stu-id="df7b5-122">When calling [**PeerGroupExportConfig**](/windows/desktop/api/P2P/nf-p2p-peergroupexportconfig), an application or API user must provide a strong password of sufficient length.</span></span> <span data-ttu-id="df7b5-123">Esto es importante porque los datos de identidad importados contienen la clave privada para el grupo.</span><span class="sxs-lookup"><span data-stu-id="df7b5-123">This is important because the imported identity data contains the private key for the group.</span></span>

 

<span data-ttu-id="df7b5-124">Para exportar la configuración actual del grupo del mismo nivel, llame a [**PeerGroupExportConfig**](/windows/desktop/api/P2P/nf-p2p-peergroupexportconfig), pasando el identificador al grupo (obtenido mediante una llamada anterior a [**PeerGroupJoin**](/windows/desktop/api/P2P/nf-p2p-peergroupjoin), [**PeerGroupOpen**](/windows/desktop/api/P2P/nf-p2p-peergroupopen)o [**PeerGroupCreate**](/windows/desktop/api/P2P/nf-p2p-peergroupcreate)) y una contraseña usada para cifrar y proteger el archivo de configuración.</span><span class="sxs-lookup"><span data-stu-id="df7b5-124">To export the current peer group configuration, call [**PeerGroupExportConfig**](/windows/desktop/api/P2P/nf-p2p-peergroupexportconfig), passing in the handle to the group (obtained by a previous call to [**PeerGroupJoin**](/windows/desktop/api/P2P/nf-p2p-peergroupjoin), [**PeerGroupOpen**](/windows/desktop/api/P2P/nf-p2p-peergroupopen), or [**PeerGroupCreate**](/windows/desktop/api/P2P/nf-p2p-peergroupcreate)), and a password used to encrypt and protect the configuration file.</span></span> <span data-ttu-id="df7b5-125">Esta función devuelve una cadena XML que contiene la configuración en el formato del siguiente ejemplo, que se puede escribir en un archivo y pasar a otro equipo mediante un mecanismo de transferencia externo, como el correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="df7b5-125">This function returns an XML string that contains the configuration in the format of the following example, which can then be written to a file and passed to another computer by using an external transfer mechanism, such as email.</span></span>

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

<span data-ttu-id="df7b5-126">Después de obtener la configuración de grupo como una cadena XML, se puede importar el grupo llamando a [**PeerGroupImportConfig**](/windows/desktop/api/P2P/nf-p2p-peergroupimportconfig) con la cadena XML de configuración y la contraseña específica proporcionada a [**PeerGroupExportConfig**](/windows/desktop/api/P2P/nf-p2p-peergroupexportconfig).</span><span class="sxs-lookup"><span data-stu-id="df7b5-126">After obtaining the group configuration as an XML string, the group can be imported by calling [**PeerGroupImportConfig**](/windows/desktop/api/P2P/nf-p2p-peergroupimportconfig) with the configuration XML string and the specific password supplied to [**PeerGroupExportConfig**](/windows/desktop/api/P2P/nf-p2p-peergroupexportconfig).</span></span> <span data-ttu-id="df7b5-127">Esta función devuelve un nombre de identidad y un nombre de grupo del mismo nivel, que se puede proporcionar a continuación a [**PeerGroupOpen**](/windows/desktop/api/P2P/nf-p2p-peergroupopen) y una conexión al grupo establecido.</span><span class="sxs-lookup"><span data-stu-id="df7b5-127">This function returns an identity name and a group peer name, which can then be supplied to [**PeerGroupOpen**](/windows/desktop/api/P2P/nf-p2p-peergroupopen) and a connection to the group established.</span></span>

 

 



