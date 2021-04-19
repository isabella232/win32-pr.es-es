---
description: Al tener acceso a un servidor de Instrumental de administración de Windows (WMI) con un script, puede elegir entre los protocolos de autenticación NT LAN Manager (NTLM) o Kerberos.
ms.assetid: db2dc750-bfdd-4f6c-859b-e104814f0800
ms.tgt_platform: multiple
title: Establecer el servicio de autenticación mediante VBScript
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: bd2cf444560aac7ebce96b52d9abaa528bdcaa76
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105717040"
---
# <a name="setting-the-authentication-service-using-vbscript"></a><span data-ttu-id="0a1d9-103">Establecer el servicio de autenticación mediante VBScript</span><span class="sxs-lookup"><span data-stu-id="0a1d9-103">Setting the Authentication Service Using VBScript</span></span>

<span data-ttu-id="0a1d9-104">Al tener acceso a un servidor de Instrumental de administración de Windows (WMI) con un script, puede elegir entre los protocolos de autenticación NT LAN Manager (NTLM) o Kerberos.</span><span class="sxs-lookup"><span data-stu-id="0a1d9-104">When accessing a Windows Management Instrumentation (WMI) server with a script, you can choose between NT LAN Manager (NTLM) or Kerberos authentication protocols.</span></span> <span data-ttu-id="0a1d9-105">No es necesario especificar Kerberos excepto cuando se usa la delegación.</span><span class="sxs-lookup"><span data-stu-id="0a1d9-105">Specifying Kerberos is not required except when using delegation.</span></span> <span data-ttu-id="0a1d9-106">Para obtener más información, vea [conectarse a un tercer equipo: Delegación](connecting-to-a-3rd-computer-delegation.md).</span><span class="sxs-lookup"><span data-stu-id="0a1d9-106">For more information, see [Connecting to a 3rd Computer-Delegation](connecting-to-a-3rd-computer-delegation.md).</span></span>

<span data-ttu-id="0a1d9-107">Dado que las versiones de sistema operativo difieren en el servicio de autenticación que usan, se recomienda no especificar un valor para el campo entidad al conectarse a un sistema remoto.</span><span class="sxs-lookup"><span data-stu-id="0a1d9-107">Because operating system versions differ in which authentication service they use, it is recommended that you do not specify a value for the authority field when connecting to a remote system.</span></span> <span data-ttu-id="0a1d9-108">En su lugar, permita que el sistema operativo y la versión distribuida del modelo de objetos componentes (DCOM) seleccionen NTLM o Kerberos.</span><span class="sxs-lookup"><span data-stu-id="0a1d9-108">Instead, allow the operating system and distributed version of Component Object Model (DCOM) to select NTLM or Kerberos.</span></span> <span data-ttu-id="0a1d9-109">Si se especifica un servicio de autenticación, la sintaxis requiere el nombre de la entidad de seguridad del servidor, que es el nombre del equipo de destino en lugar del controlador de dominio.</span><span class="sxs-lookup"><span data-stu-id="0a1d9-109">If an authentication service is specified, the syntax requires the server principal name, which is the name of the target computer rather than the domain controller.</span></span>

<span data-ttu-id="0a1d9-110">Solo puede usar el parámetro Authority con conexiones a servidores WMI remotos.</span><span class="sxs-lookup"><span data-stu-id="0a1d9-110">You can use the authority parameter only with connections to remote WMI servers.</span></span> <span data-ttu-id="0a1d9-111">Se produce un error en el intento de conexión si intenta establecer los niveles de autorización como parte de un moniker o con una llamada a [**SWbemLocator. ConnectServer**](swbemlocator-connectserver.md) para una conexión local.</span><span class="sxs-lookup"><span data-stu-id="0a1d9-111">The connection attempt fails if you attempt to set authorization levels as part of a moniker or with a call to [**SWbemLocator.ConnectServer**](swbemlocator-connectserver.md) for a local connection.</span></span>

<span data-ttu-id="0a1d9-112">Realice el procedimiento siguiente para especificar el servicio de autenticación que desea usar en el parámetro *strAuthority* del método [**SWbemLocator. ConnectServer**](swbemlocator-connectserver.md) o la conexión de cadena de [moniker](constructing-a-moniker-string.md) .</span><span class="sxs-lookup"><span data-stu-id="0a1d9-112">Perform the following procedure to specify the authentication service that you want to use in the *strAuthority* parameter of the [**SWbemLocator.ConnectServer**](swbemlocator-connectserver.md) method or the [moniker](constructing-a-moniker-string.md) string connection.</span></span>

<span data-ttu-id="0a1d9-113">**Para especificar la autenticación NTLM o Kerberos con la API de scripting para WMI**</span><span class="sxs-lookup"><span data-stu-id="0a1d9-113">**To specify NTLM or Kerberos authentication with the Scripting API for WMI**</span></span>

1.  <span data-ttu-id="0a1d9-114">Si el parámetro *strAuthority* comienza con la cadena "Kerberos:", WMI supone que la cadena hace referencia a un nombre de entidad de seguridad de Kerberos y se utiliza la autenticación Kerberos.</span><span class="sxs-lookup"><span data-stu-id="0a1d9-114">If the *strAuthority* parameter begins with the string "kerberos:", WMI assumes the string refers to a Kerberos principal name and Kerberos authentication is used.</span></span> <span data-ttu-id="0a1d9-115">Si el parámetro *strAuthority* comienza con la cadena "ntlmdomain:", WMI utiliza la autenticación NTLM en su lugar.</span><span class="sxs-lookup"><span data-stu-id="0a1d9-115">If the *strAuthority* parameter begins with the string "ntlmdomain:", WMI uses NTLM authentication instead.</span></span>
2.  <span data-ttu-id="0a1d9-116">Como alternativa, puede usar la parte de autoridad de un moniker para especificar el tipo de autenticación que se utiliza para conectarse a WMI.</span><span class="sxs-lookup"><span data-stu-id="0a1d9-116">Alternately, You can use the authority part of a moniker to specify the type of authentication used to connect to WMI.</span></span> <span data-ttu-id="0a1d9-117">Para usar la autenticación Kerberos al utilizar un moniker, incluya la cadena "Authority = Kerberos:" seguida del nombre de la entidad de seguridad.</span><span class="sxs-lookup"><span data-stu-id="0a1d9-117">To use Kerberos authentication when using a moniker include the string, "authority=kerberos:" followed by the principal name.</span></span> <span data-ttu-id="0a1d9-118">Para usar la autenticación NTLM, incluya la cadena "Authority = ntlmdomain:" seguida del nombre de dominio NTLM.</span><span class="sxs-lookup"><span data-stu-id="0a1d9-118">To use NTLM authentication, include the string, "authority=ntlmdomain:" followed by the NTLM domain name.</span></span>

    <span data-ttu-id="0a1d9-119">En el ejemplo siguiente se muestra un moniker que solicita la autenticación Kerberos mediante la entidad "midominio \\ Server".</span><span class="sxs-lookup"><span data-stu-id="0a1d9-119">The following example shows you a moniker that requests Kerberos authentication using the principal "mydomain\\server".</span></span>

    ```VB
    winmgmts:{impersonationLevel=delegate, _
            authority=kerberos:mydomain\server} _
            !//myserver/root/default:__cimomidentification=@
    ```

    

    <span data-ttu-id="0a1d9-120">En cambio, en el ejemplo siguiente se muestra un moniker que solicita la autenticación NTLM mediante el dominio "midominio".</span><span class="sxs-lookup"><span data-stu-id="0a1d9-120">In contrast, the following example shows you a moniker that requests NTLM authentication using the domain "mydomain".</span></span>

    ```VB
    winmgmts:{impersonationLevel=impersonate, _
            authority=ntlmdomain:mydomain} _
            !//myserver/root/default:__cimomidentification=@
    ```

    

 

 



