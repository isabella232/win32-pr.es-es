---
title: Usar cmdlets de WMI de Windows PowerShell para administrar el servidor de BITS Compact
description: Windows PowerShell proporciona un mecanismo sencillo para conectarse a Instrumental de administración de Windows (WMI) en un equipo remoto y administrar el servidor de Servicio de transferencia inteligente en segundo plano (BITS) Compact.
ms.assetid: fe174d2f-4ca0-431e-b1b8-1893ec54147a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6c3c942672c147ec5daa0caa2a370e487be80809
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "103995424"
---
# <a name="using-wmi-windows-powershell-cmdlets-to-manage-the-bits-compact-server"></a><span data-ttu-id="846c4-103">Usar cmdlets de WMI de Windows PowerShell para administrar el servidor de BITS Compact</span><span class="sxs-lookup"><span data-stu-id="846c4-103">Using WMI Windows PowerShell Cmdlets to Manage the BITS Compact Server</span></span>

<span data-ttu-id="846c4-104">Windows PowerShell proporciona un mecanismo sencillo para conectarse a Instrumental de administración de Windows (WMI) en un equipo remoto y administrar el servidor de Servicio de transferencia inteligente en segundo plano (BITS) Compact.</span><span class="sxs-lookup"><span data-stu-id="846c4-104">Windows PowerShell provides a simple mechanism to connect to Windows Management Instrumentation (WMI) on a remote computer and manage the Background Intelligent Transfer Service (BITS) Compact Server.</span></span> <span data-ttu-id="846c4-105">El servidor BITS Compact es un componente de servidor opcional que se debe instalar por separado.</span><span class="sxs-lookup"><span data-stu-id="846c4-105">The BITS Compact Server is an optional server component that must be installed separately.</span></span> <span data-ttu-id="846c4-106">Para obtener información acerca de cómo instalar el servidor compacto, consulte la documentación del [servidor de bits Compact](bits-compact-server.md) .</span><span class="sxs-lookup"><span data-stu-id="846c4-106">For information about installing the Compact Server, see the [BITS Compact Server](bits-compact-server.md) documentation.</span></span>

1.  <span data-ttu-id="846c4-107">Conéctese al proveedor BITS.</span><span class="sxs-lookup"><span data-stu-id="846c4-107">Connect to the BITS provider.</span></span>

    ```PowerShell
    $cred = Get-Credential
    $bcs = Get-WmiObject -Namespace "root\Microsoft\BITS" -Class "BITSCompactServerUrlGroup" `
    -List -ComputerName Server1 -Credential $cred
    ```

    

    <span data-ttu-id="846c4-108">El cmdlet [Get-Credential](/previous-versions//dd315327(v=technet.10)) solicita las credenciales del usuario para conectarse al equipo remoto y asigna las credenciales al objeto $cred.</span><span class="sxs-lookup"><span data-stu-id="846c4-108">The [Get-Credential](/previous-versions//dd315327(v=technet.10)) cmdlet requests the user's credentials to connect to the remote computer and assigns the credentials to the $cred object.</span></span>

    <span data-ttu-id="846c4-109">Los objetos devueltos por el cmdlet [Get-WMIObject](/previous-versions//dd315295(v=technet.10)) se asignan a la variable $BCS.</span><span class="sxs-lookup"><span data-stu-id="846c4-109">The objects returned by the [Get-WmiObject](/previous-versions//dd315295(v=technet.10)) cmdlet are assigned to the $bcs variable.</span></span> <span data-ttu-id="846c4-110">En el ejemplo anterior, el cmdlet [Get-WMIObject](/previous-versions//dd315295(v=technet.10)) recupera la clase [BITSCompactServerUrlGroup](/previous-versions/windows/desktop/bitsprov/bitslightweightserverurlgroup) en el \\ \\ espacio de nombres de Microsoft bits raíz de server1.</span><span class="sxs-lookup"><span data-stu-id="846c4-110">In the preceding example, the [Get-WmiObject](/previous-versions//dd315295(v=technet.10)) cmdlet retrieves the [BITSCompactServerUrlGroup](/previous-versions/windows/desktop/bitsprov/bitslightweightserverurlgroup) class in the root\\Microsoft\\BITS namespace of Server1.</span></span> <span data-ttu-id="846c4-111">Se puede llamar a los métodos estáticos expuestos por la clase [BITSCompactServerUrlGroup](/previous-versions/windows/desktop/bitsprov/bitslightweightserverurlgroup) en el objeto $BCS.</span><span class="sxs-lookup"><span data-stu-id="846c4-111">Static methods exposed by the [BITSCompactServerUrlGroup](/previous-versions/windows/desktop/bitsprov/bitslightweightserverurlgroup) class can be called on the $bcs object.</span></span> <span data-ttu-id="846c4-112">Para obtener más información acerca de la administración remota de BITS, consulte [clases]( /previous-versions//dd904507(v=vs.85))de proveedor bits [y proveedor bits](/previous-versions/windows/desktop/bitsprov/bits-provider) .</span><span class="sxs-lookup"><span data-stu-id="846c4-112">For more information about BITS remote management, see [BITS provider](/previous-versions/windows/desktop/bitsprov/bits-provider) and [BITS provider classes]( /previous-versions//dd904507(v=vs.85)).</span></span>

    > [!Note]  
    > <span data-ttu-id="846c4-113">El carácter de acento grave ( \` ) se usa para indicar un salto de línea.</span><span class="sxs-lookup"><span data-stu-id="846c4-113">The grave-accent character (\`) is used to indicate a line break.</span></span>

     

2.  <span data-ttu-id="846c4-114">Cree un grupo de direcciones URL en el servidor.</span><span class="sxs-lookup"><span data-stu-id="846c4-114">Create a URL group on the server.</span></span>

    ```PowerShell
    $URLGroup = "https://Server1:80/testurlgroup" 
    $bcs.CreateUrlGroup($URLGroup)
    ```

    

    <span data-ttu-id="846c4-115">La https://Server1:80/testurlgroup cadena de prefijo de dirección URL "" se asigna a la variable $URLGroup.</span><span class="sxs-lookup"><span data-stu-id="846c4-115">The "https://Server1:80/testurlgroup" URL prefix string is assigned to the $URLGroup variable.</span></span> <span data-ttu-id="846c4-116">La variable $URLGroup se pasa al método [CreateUrlGroup](/previous-versions/windows/desktop/bitsprov/createurlgroup-bitslightweightserverurlgroup) , que crea el grupo de direcciones URL en server1.</span><span class="sxs-lookup"><span data-stu-id="846c4-116">The $URLGroup variable is passed to the [CreateUrlGroup](/previous-versions/windows/desktop/bitsprov/createurlgroup-bitslightweightserverurlgroup) method, which creates the URL group on Server1.</span></span>

    <span data-ttu-id="846c4-117">Puede especificar un grupo de direcciones URL diferente.</span><span class="sxs-lookup"><span data-stu-id="846c4-117">You can specify a different URL group.</span></span> <span data-ttu-id="846c4-118">El grupo de direcciones URL debe ajustarse a una cadena de prefijo de dirección URL válida.</span><span class="sxs-lookup"><span data-stu-id="846c4-118">The URL group must conform to a valid URL prefix string.</span></span> <span data-ttu-id="846c4-119">Para obtener más información sobre los prefijos de dirección URL, vea [UrlPrefix Strings](../http/urlprefix-strings.md).</span><span class="sxs-lookup"><span data-stu-id="846c4-119">For more information about URL prefixes, see [UrlPrefix Strings](../http/urlprefix-strings.md).</span></span>

3.  <span data-ttu-id="846c4-120">Hospede un archivo en el grupo de direcciones URL.</span><span class="sxs-lookup"><span data-stu-id="846c4-120">Host a file on the URL group.</span></span>

    ```PowerShell
    $bcsObj = Get-WmiObject -Namespace "root\Microsoft\BITS" -Class "BITSCompactServerUrlGroup" -filter ("UrlGroup='" + $URLGroup + "'") -ComputerName Server1 -Credential $cred
    $bcsObj.CreateURL("url.txt", "c:\\temp\\1.txt", "") -ComputerName Server1 -Credential $cred
    ```

    

    <span data-ttu-id="846c4-121">La instancia de BITSCompactServerUrlGroup devuelta por el cmdlet [Get-WMIObject](/previous-versions//dd315295(v=technet.10)) se asigna a la variable $bcsObj.</span><span class="sxs-lookup"><span data-stu-id="846c4-121">The BITSCompactServerUrlGroup instance returned by the [Get-WmiObject](/previous-versions//dd315295(v=technet.10)) cmdlet is assigned to the $bcsObj variable.</span></span> <span data-ttu-id="846c4-122">Se llama al método [CreateUrl](/previous-versions/windows/desktop/bitsprov/createurl-bitslightweightserverurlgroup) para el $bcsObj con el sufijo de dirección URL "url.txt", la \\ \\ ruta de acceso de origen "c: Temp \\ \\1.txt" para el archivo y una cadena de descriptor de seguridad vacía como parámetros.</span><span class="sxs-lookup"><span data-stu-id="846c4-122">The [CreateUrl](/previous-versions/windows/desktop/bitsprov/createurl-bitslightweightserverurlgroup) method is called for the $bcsObj with the "url.txt" URL suffix, the "c:\\\\temp\\\\1.txt" source path for the file, and an empty security descriptor string as parameters.</span></span> <span data-ttu-id="846c4-123">El sufijo "url.txt" se agrega al prefijo del grupo de direcciones URL.</span><span class="sxs-lookup"><span data-stu-id="846c4-123">The "url.txt" suffix is added to the URL group prefix.</span></span> <span data-ttu-id="846c4-124">Los clientes pueden descargar el archivo de la siguiente dirección: https://Server1:80/testurlgroup/url.txt .</span><span class="sxs-lookup"><span data-stu-id="846c4-124">Clients can download the file from the following address: https://Server1:80/testurlgroup/url.txt.</span></span>

4.  <span data-ttu-id="846c4-125">Limpie la dirección URL y el grupo de direcciones URL.</span><span class="sxs-lookup"><span data-stu-id="846c4-125">Clean up the URL and the URL group.</span></span>

    ```PowerShell
    $bcsObj.Delete()
    ```

    

    <span data-ttu-id="846c4-126">El método **System. Object Delete** elimina el objeto de $bcsObj.</span><span class="sxs-lookup"><span data-stu-id="846c4-126">The **system.object Delete** method deletes the $bcsObj object.</span></span>

## <a name="related-topics"></a><span data-ttu-id="846c4-127">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="846c4-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="846c4-128">Servidor BITS compacto</span><span class="sxs-lookup"><span data-stu-id="846c4-128">BITS Compact Server</span></span>](./bits-compact-server.md)
</dt> <dt>

[<span data-ttu-id="846c4-129">Proveedor BITS</span><span class="sxs-lookup"><span data-stu-id="846c4-129">BITS provider</span></span>](/previous-versions/windows/desktop/bitsprov/bits-provider)
</dt> <dt>

<span data-ttu-id="846c4-130">[Clases de proveedor BITS]( /previous-versions//dd904507(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="846c4-130">[BITS provider classes]( /previous-versions//dd904507(v=vs.85))</span></span>
</dt> <dt>

<span data-ttu-id="846c4-131">[Get-Credential](/previous-versions//dd315327(v=technet.10))</span><span class="sxs-lookup"><span data-stu-id="846c4-131">[Get-Credential](/previous-versions//dd315327(v=technet.10))</span></span>
</dt> <dt>

<span data-ttu-id="846c4-132">[Get-WmiObject](/previous-versions//dd315295(v=technet.10))</span><span class="sxs-lookup"><span data-stu-id="846c4-132">[Get-WmiObject](/previous-versions//dd315295(v=technet.10))</span></span>
</dt> </dl>

 

 