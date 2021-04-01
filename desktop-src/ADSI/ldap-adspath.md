---
title: ADsPath de LDAP
description: En este tema se muestra la sintaxis que se debe usar para la ADsPath de LDAP.
ms.assetid: adacf6af-8683-4c3c-91bf-9489f2d5d817
ms.tgt_platform: multiple
keywords:
- ADsPath de LDAP
- ADsPath, LDAP, descripción
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1728d2531bb2043f95e5896e67ec054095f2595a
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/21/2020
ms.locfileid: "103793881"
---
# <a name="ldap-adspath"></a><span data-ttu-id="1ebd7-105">ADsPath de LDAP</span><span class="sxs-lookup"><span data-stu-id="1ebd7-105">LDAP ADsPath</span></span>

<span data-ttu-id="1ebd7-106">El atributo ADsPath del proveedor LDAP de Microsoft requiere el formato siguiente.</span><span class="sxs-lookup"><span data-stu-id="1ebd7-106">The Microsoft LDAP provider ADsPath requires the following format.</span></span>


```C++
LDAP://HostName[:PortNumber][/DistinguishedName]
```



> [!Note]  
> <span data-ttu-id="1ebd7-107">Los caracteres de corchete de apertura y cierre ( \[ \] ) indican parámetros opcionales; no es una parte literal de la cadena de enlace.</span><span class="sxs-lookup"><span data-stu-id="1ebd7-107">The left and right bracket characters (\[ \]) indicate optional parameters; it is not a literal part of the binding string.</span></span>

 

<span data-ttu-id="1ebd7-108">El "nombre de host" puede ser un nombre de equipo, una dirección IP o un nombre de dominio.</span><span class="sxs-lookup"><span data-stu-id="1ebd7-108">The "HostName" can be a computer name, an IP address, or a domain name.</span></span> <span data-ttu-id="1ebd7-109">También se puede especificar un nombre de servidor en la cadena de enlace.</span><span class="sxs-lookup"><span data-stu-id="1ebd7-109">A server name can also be specified in the binding string.</span></span> <span data-ttu-id="1ebd7-110">La mayoría de los proveedores LDAP siguen un modelo que requiere que se especifique un nombre de servidor.</span><span class="sxs-lookup"><span data-stu-id="1ebd7-110">Most LDAP providers follow a model that requires a server name to be specified.</span></span>

<span data-ttu-id="1ebd7-111">El "númeroDePuerto" especifica el puerto que se va a utilizar para la conexión.</span><span class="sxs-lookup"><span data-stu-id="1ebd7-111">The "PortNumber" specifies the port to be used for the connection.</span></span> <span data-ttu-id="1ebd7-112">Si no se especifica ningún número de puerto, el proveedor LDAP utiliza el número de puerto predeterminado.</span><span class="sxs-lookup"><span data-stu-id="1ebd7-112">If no port number is specified, the LDAP provider uses the default port number.</span></span> <span data-ttu-id="1ebd7-113">El número de puerto predeterminado es 389 si no se usa una conexión SSL o 636 si se usa una conexión SSL.</span><span class="sxs-lookup"><span data-stu-id="1ebd7-113">The default port number is 389 if not using an SSL connection or 636 if using an SSL connection.</span></span>

<span data-ttu-id="1ebd7-114">"DistinguishedName" especifica el nombre distintivo de un objeto concreto.</span><span class="sxs-lookup"><span data-stu-id="1ebd7-114">The "DistinguishedName" specifies the distinguished name of a specific object.</span></span> <span data-ttu-id="1ebd7-115">Se garantiza que un nombre distintivo de un objeto determinado es único.</span><span class="sxs-lookup"><span data-stu-id="1ebd7-115">A distinguished name for a given object is guaranteed to be unique.</span></span>

<span data-ttu-id="1ebd7-116">En la tabla siguiente se muestran ejemplos de cadenas de enlace.</span><span class="sxs-lookup"><span data-stu-id="1ebd7-116">The following table lists examples of binding strings.</span></span>



| <span data-ttu-id="1ebd7-117">Ejemplo de ADsPath de LDAP</span><span class="sxs-lookup"><span data-stu-id="1ebd7-117">LDAP ADsPath example</span></span>                                      | <span data-ttu-id="1ebd7-118">Descripción</span><span class="sxs-lookup"><span data-stu-id="1ebd7-118">Description</span></span>                                                |
|-----------------------------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="1ebd7-119">LDAP</span><span class="sxs-lookup"><span data-stu-id="1ebd7-119">LDAP:</span></span>                                                     | <span data-ttu-id="1ebd7-120">Enlazar a la raíz del espacio de nombres LDAP.</span><span class="sxs-lookup"><span data-stu-id="1ebd7-120">Bind to the root of the LDAP namespace.</span></span>                    |
| <span data-ttu-id="1ebd7-121">LDAP://server01</span><span class="sxs-lookup"><span data-stu-id="1ebd7-121">LDAP://server01</span></span>                                           | <span data-ttu-id="1ebd7-122">Enlazar a un servidor específico.</span><span class="sxs-lookup"><span data-stu-id="1ebd7-122">Bind to a specific server.</span></span>                                 |
| <span data-ttu-id="1ebd7-123">LDAP://server01:390</span><span class="sxs-lookup"><span data-stu-id="1ebd7-123">LDAP://server01:390</span></span>                                       | <span data-ttu-id="1ebd7-124">Enlazar a un servidor específico usando el número de puerto especificado.</span><span class="sxs-lookup"><span data-stu-id="1ebd7-124">Bind to a specific server using the specified port number.</span></span> |
| <span data-ttu-id="1ebd7-125">LDAP:Rio de la siguiente Juan Smith, CN = users, DC = Fabrikam, DC = com</span><span class="sxs-lookup"><span data-stu-id="1ebd7-125">LDAP://CN=Jeff Smith,CN=users,DC=fabrikam,DC=com</span></span>          | <span data-ttu-id="1ebd7-126">Enlazar a un objeto específico.</span><span class="sxs-lookup"><span data-stu-id="1ebd7-126">Bind to a specific object.</span></span>                                 |
| <span data-ttu-id="1ebd7-127">LDAP://server01/CN=Jeff Smith, CN = users, DC = Fabrikam, DC = com</span><span class="sxs-lookup"><span data-stu-id="1ebd7-127">LDAP://server01/CN=Jeff Smith,CN=users,DC=fabrikam,DC=com</span></span> | <span data-ttu-id="1ebd7-128">Enlazar a un objeto específico a través de un servidor específico.</span><span class="sxs-lookup"><span data-stu-id="1ebd7-128">Bind to a specific object through a specific server.</span></span>       |



 

<span data-ttu-id="1ebd7-129">Si se requiere la autenticación Kerberos para la finalización correcta de una solicitud de directorio específica, la cadena de enlace debe usar una ADsPath sin servidor, como LDAP: encontrada = Jeff Smith, CN = users, DC = Fabrikam, DC = com o debe usar una ADsPath con un nombre de servidor DNS completo, como LDAP://server01.fabrikam.com/CN=Jeff Smith, CN = users, DC = Fabrikam, DC = com.</span><span class="sxs-lookup"><span data-stu-id="1ebd7-129">If Kerberos authentication is required for the successful completion of a specific directory request, the binding string must use either a serverless ADsPath, such as LDAP://CN=Jeff Smith,CN=users,DC=fabrikam,DC=com, or it must use an ADsPath with a fully qualified DNS server name, such as LDAP://server01.fabrikam.com/CN=Jeff Smith,CN=users,DC=fabrikam,DC=com.</span></span> <span data-ttu-id="1ebd7-130">No se garantiza que el enlace al servidor mediante un nombre NETBIOS plano o un nombre DNS corto, por ejemplo, con el nombre Server01 en lugar de server01.fabrikam.com, produzca la autenticación Kerberos.</span><span class="sxs-lookup"><span data-stu-id="1ebd7-130">Binding to the server using a flat NETBIOS name or a short DNS name, for example, using the name server01 instead of server01.fabrikam.com, is not guaranteed to yield Kerberos authentication.</span></span>

<span data-ttu-id="1ebd7-131">Para obtener más información y ejemplos de cadenas de enlace LDAP, así como una descripción de los caracteres especiales que se pueden usar en las cadenas de enlace LDAP, vea ADsPath de LDAP.</span><span class="sxs-lookup"><span data-stu-id="1ebd7-131">For more information and examples of LDAP binding strings, as well as a description of special characters that can be used in LDAP binding strings, see LDAP ADsPath.</span></span>

<span data-ttu-id="1ebd7-132">**Windows 2000 con SP1 y versiones posteriores:** Con el proveedor LDAP, si una cadena de enlace incluye un nombre de servidor, puede aumentar el rendimiento mediante el uso del marcador de **\_ \_ enlace del servidor ADS** con la función [**ADsOpenObject**](/windows/desktop/api/Adshlp/nf-adshlp-adsopenobject) o el método [**IADsOpenDSObject:: OpenDSObject**](/windows/desktop/api/Iads/nf-iads-iadsopendsobject-opendsobject) .</span><span class="sxs-lookup"><span data-stu-id="1ebd7-132">**Windows 2000 with SP1 and later:** With the LDAP provider, if a binding string includes a server name, you can increase performance by using the **ADS\_SERVER\_BIND** flag with the [**ADsOpenObject**](/windows/desktop/api/Adshlp/nf-adshlp-adsopenobject) function or the [**IADsOpenDSObject::OpenDSObject**](/windows/desktop/api/Iads/nf-iads-iadsopendsobject-opendsobject) method.</span></span> <span data-ttu-id="1ebd7-133">La marca de **\_ \_ enlace del servidor de ADS** indica que se especificó un nombre de servidor, lo que permite que ADSI Evite tráfico de red adicional e innecesario.</span><span class="sxs-lookup"><span data-stu-id="1ebd7-133">The **ADS\_SERVER\_BIND** flag indicates that a server name was specified, which enables ADSI to avoid additional, unnecessary network traffic.</span></span>

## <a name="ldap-special-characters"></a><span data-ttu-id="1ebd7-134">Caracteres especiales LDAP</span><span class="sxs-lookup"><span data-stu-id="1ebd7-134">LDAP Special Characters</span></span>

<span data-ttu-id="1ebd7-135">LDAP tiene varios caracteres especiales que se reservan para su uso con la API de LDAP.</span><span class="sxs-lookup"><span data-stu-id="1ebd7-135">LDAP has several special characters which are reserved for use by the LDAP API.</span></span> <span data-ttu-id="1ebd7-136">La lista de caracteres especiales puede encontrarse en [nombres distintivos](/previous-versions/windows/desktop/ldap/distinguished-names).</span><span class="sxs-lookup"><span data-stu-id="1ebd7-136">The list of special characters can be found in [Distinguished Names](/previous-versions/windows/desktop/ldap/distinguished-names).</span></span> <span data-ttu-id="1ebd7-137">Para usar uno de estos caracteres en una ADsPath sin generar un error, el carácter debe ir precedido de un carácter de barra diagonal inversa ( \\ ).</span><span class="sxs-lookup"><span data-stu-id="1ebd7-137">To use one of these characters in an ADsPath without generating an error, the character must be preceded by a backslash (\\) character.</span></span> <span data-ttu-id="1ebd7-138">Esto se conoce como *escapar* del carácter.</span><span class="sxs-lookup"><span data-stu-id="1ebd7-138">This is known as *escaping* the character.</span></span> <span data-ttu-id="1ebd7-139">Por ejemplo, si se proporciona un nombre de usuario con el formato " <last name> , <first name> ", la coma del valor de nombre debe ser de escape.</span><span class="sxs-lookup"><span data-stu-id="1ebd7-139">For example, if a user name is given in the form of "<last name>,<first name>", the comma in the name value must be escaped.</span></span> <span data-ttu-id="1ebd7-140">La cadena resultante tendría el siguiente aspecto:</span><span class="sxs-lookup"><span data-stu-id="1ebd7-140">The resulting string would look like this:</span></span>


```C++
LDAP://CN=Smith\,Jeff,CN=users,DC=fabrikam,DC=com
```



<span data-ttu-id="1ebd7-141">El carácter de escape también se puede especificar mediante el código de carácter hexadecimal de dos dígitos.</span><span class="sxs-lookup"><span data-stu-id="1ebd7-141">The escaped character can also be specified by its two digit hexadecimal character code.</span></span> <span data-ttu-id="1ebd7-142">Esto se muestra en el ejemplo siguiente.</span><span class="sxs-lookup"><span data-stu-id="1ebd7-142">This is shown in the following example.</span></span>


```C++
LDAP://CN=Smith\2CJeff,CN=users,DC=fabrikam,DC=com
```



<span data-ttu-id="1ebd7-143">Los caracteres no imprimibles, como el avance de línea y el retorno de carro, deben ser de escape y se pueden especificar mediante el código de carácter hexadecimal de dos dígitos.</span><span class="sxs-lookup"><span data-stu-id="1ebd7-143">Non-printable characters, such as the line feed and carriage return, must be escaped and specified by their two digit hexadecimal character code.</span></span> <span data-ttu-id="1ebd7-144">Esto se muestra en el ejemplo siguiente.</span><span class="sxs-lookup"><span data-stu-id="1ebd7-144">This is shown in the following example.</span></span>


```C++
LDAP://CN=Line\0AFeed,CN=users,DC=fabrikam,DC=com
```



## <a name="for-more-information"></a><span data-ttu-id="1ebd7-145">Para obtener más información</span><span class="sxs-lookup"><span data-stu-id="1ebd7-145">For More Information</span></span>

<span data-ttu-id="1ebd7-146">Para obtener más información acerca de la notación de nombre distintivo utilizada por los servicios de directorio compatibles con LDAP, vea [https://www.ietf.org/rfc/rfc1779.txt](https://www.ietf.org/rfc/rfc1779.txt) .</span><span class="sxs-lookup"><span data-stu-id="1ebd7-146">For more information about the distinguished name notation used by LDAP-compliant directory services, see [https://www.ietf.org/rfc/rfc1779.txt](https://www.ietf.org/rfc/rfc1779.txt).</span></span>

 

 