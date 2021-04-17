---
description: Puede requerir que los scripts y las aplicaciones de cliente establezcan una conexión cifrada para la autenticación agregando el calificador RequiresEncryption al archivo Managed Object Format (MOF). mof que crea el espacio de nombres.
ms.assetid: 07b225a2-3834-4879-beae-f5b9180d112f
ms.tgt_platform: multiple
title: Requerir una conexión cifrada a un espacio de nombres
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e42415c0f714f99a51d6a1a0ee1a0b22f398b1b7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105697732"
---
# <a name="requiring-an-encrypted-connection-to-a-namespace"></a><span data-ttu-id="29479-103">Requerir una conexión cifrada a un espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="29479-103">Requiring an Encrypted Connection to a Namespace</span></span>

<span data-ttu-id="29479-104">Puede requerir que los scripts y las aplicaciones de cliente establezcan una conexión cifrada para la autenticación agregando el calificador **RequiresEncryption** al archivo Managed Object Format (MOF). mof que crea el espacio de nombres.</span><span class="sxs-lookup"><span data-stu-id="29479-104">You can require that client scripts and applications establish an encrypted connection for authentication by adding the **RequiresEncryption** qualifier to the Managed Object Format (MOF) .mof file that creates the namespace.</span></span>


<span data-ttu-id="29479-105">Una conexión cifrada a un espacio de nombres WMI especifica la **\_ \_ \_ \_ \_ privacidad de nivel de autenticación de RPC C** (o **PktPrivacy** en un script) para la autenticación.</span><span class="sxs-lookup"><span data-stu-id="29479-105">An encrypted connection to a WMI namespace specifies **RPC\_C\_AUTHN\_LEVEL\_PKT\_PRIVACY** (or **PktPrivacy** in a script) for authentication.</span></span> <span data-ttu-id="29479-106">El calificador **RequiresEncryption** hace que WMI rechace las solicitudes de datos entrantes a menos que utilicen explícitamente la autenticación cifrada.</span><span class="sxs-lookup"><span data-stu-id="29479-106">The **RequiresEncryption** qualifier causes WMI to reject any incoming data requests unless they explicitly use encrypted authentication.</span></span> <span data-ttu-id="29479-107">Para obtener más información, vea [establecer el nivel de seguridad de proceso predeterminado mediante VBScript](setting-the-default-process-security-level-using-vbscript.md) o [establecer la autenticación con C++](setting-authentication-using-c-.md).</span><span class="sxs-lookup"><span data-stu-id="29479-107">For more information, see [Setting the Default Process Security Level Using VBScript](setting-the-default-process-security-level-using-vbscript.md) or [Setting Authentication Using C++](setting-authentication-using-c-.md).</span></span>

<span data-ttu-id="29479-108">También puede modificar un espacio de nombres existente agregando este atributo y, a continuación, compilar de nuevo el archivo MOF.</span><span class="sxs-lookup"><span data-stu-id="29479-108">You can also modify an existing namespace by adding this attribute and then compile the MOF file again.</span></span> <span data-ttu-id="29479-109">**RequiresEncryption** se utiliza en [*MOF*](gloss-m.md) con la instrucción de preprocesador de [espacio de nombres pragma](pragma-namespace.md) .</span><span class="sxs-lookup"><span data-stu-id="29479-109">**RequiresEncryption** is used in [*MOF*](gloss-m.md) with the [pragma namespace](pragma-namespace.md) preprocessor instruction.</span></span>

<span data-ttu-id="29479-110">En el procedimiento siguiente se establece el espacio de nombres para requerir una conexión cifrada.</span><span class="sxs-lookup"><span data-stu-id="29479-110">The following procedure sets the namespace to require an encrypted connection.</span></span>

<span data-ttu-id="29479-111">**Para establecer el cifrado necesario**</span><span class="sxs-lookup"><span data-stu-id="29479-111">**To set required encryption**</span></span>

1.  <span data-ttu-id="29479-112">Cree un archivo Managed Object Format (MOF) o modifique el archivo MOF existente que define el espacio de nombres.</span><span class="sxs-lookup"><span data-stu-id="29479-112">Create a Managed Object Format (MOF) file or modify your existing MOF file that defines the namespace.</span></span>

    <span data-ttu-id="29479-113">En el ejemplo de código siguiente se muestra que el espacio de nombres que se va a modificar es la *raíz \\ myNameSpace* y el archivo se denomina *myNameSpace \_ Security. mof*.</span><span class="sxs-lookup"><span data-stu-id="29479-113">The following code example shows the namespace that will be modified is *root\\MyNamespace* and the file is named *MyNamespace\_security.mof*.</span></span> <span data-ttu-id="29479-114">**RequiresEncryption** tiene un tipo de valor Boolean, por lo que debe establecerse en **true** o **false**.</span><span class="sxs-lookup"><span data-stu-id="29479-114">**RequiresEncryption** has a Boolean datatype so it must be set to **True** or **False**.</span></span>

    ```mof
    #pragma namespace("\\\\.\\Root\\MyNamespace") 

    [RequiresEncryption(TRUE)] 
    instance of __systemSecurity { };
    ```

    

2.  <span data-ttu-id="29479-115">Ejecute [**mofcomp.exe**](mofcomp.md) para compilar el archivo MOF.</span><span class="sxs-lookup"><span data-stu-id="29479-115">Run [**mofcomp.exe**](mofcomp.md) to compile the MOF file.</span></span>

    <span data-ttu-id="29479-116">**c: \\ MOFCOMP myNameSpace \_ Security. mof**</span><span class="sxs-lookup"><span data-stu-id="29479-116">**c:\\mofcomp MyNamespace\_security.mof**</span></span>

    <span data-ttu-id="29479-117">En C++, utilice los métodos [**IMoFCompiler**](/windows/desktop/api/Wbemcli/nn-wbemcli-imofcompiler) .</span><span class="sxs-lookup"><span data-stu-id="29479-117">In C++, use the [**IMoFCompiler**](/windows/desktop/api/Wbemcli/nn-wbemcli-imofcompiler) methods.</span></span>

<span data-ttu-id="29479-118">WMI rechaza un cliente que utiliza el nivel de autenticación predeterminado, ya que DCOM negocia la seguridad al nivel requerido por el proceso SVCHOST en el que se ejecuta el servicio WMI.</span><span class="sxs-lookup"><span data-stu-id="29479-118">WMI rejects a client that uses the default authentication level because DCOM negotiates the security to the level required by the SVCHOST process in which the WMI service is running.</span></span> <span data-ttu-id="29479-119">Para obtener más información sobre los hosts de servicio, consulte [hospedaje y seguridad de proveedores](provider-hosting-and-security.md).</span><span class="sxs-lookup"><span data-stu-id="29479-119">For more information about service hosts, see [Provider Hosting and Security](provider-hosting-and-security.md).</span></span> <span data-ttu-id="29479-120">Para obtener más información acerca de cómo establecer los niveles de autenticación al conectarse a los espacios de nombres de WMI, vea [establecer el nivel de seguridad de proceso predeterminado con c++](setting-the-default-process-security-level-using-c-.md), [establecer la autenticación con c++](setting-authentication-using-c-.md)o [establecer el nivel de seguridad de proceso predeterminado con VBScript](setting-the-default-process-security-level-using-vbscript.md).</span><span class="sxs-lookup"><span data-stu-id="29479-120">For more information about setting authentication levels when connecting to WMI namespaces, see [Setting the Default Process Security Level Using C++](setting-the-default-process-security-level-using-c-.md), [Setting Authentication Using C++](setting-authentication-using-c-.md), or [Setting the Default Process Security Level Using VBScript](setting-the-default-process-security-level-using-vbscript.md).</span></span>

<span data-ttu-id="29479-121">Cuando se devuelven datos en una conexión de devolución de llamada asincrónica, WMI devuelve un mensaje de acceso denegado al equipo que lo solicita.</span><span class="sxs-lookup"><span data-stu-id="29479-121">When returning data on an asynchronous callback connection, WMI returns an access denied message to the requesting computer.</span></span> <span data-ttu-id="29479-122">WMI también crea una entrada de registro en el registro de eventos de NT del equipo con el espacio de nombres cifrado que indica que no se puede establecer una conexión segura con el cliente.</span><span class="sxs-lookup"><span data-stu-id="29479-122">WMI also makes a log entry in the NT Event Log of the computer with the encrypted namespace stating that a secure connection cannot be established to the client.</span></span>

<span data-ttu-id="29479-123">A partir de Windows Vista, el archivo WbemCore. log ya no existe.</span><span class="sxs-lookup"><span data-stu-id="29479-123">Starting with Windows Vista, the WbemCore.log file no longer exists.</span></span> <span data-ttu-id="29479-124">Puede buscar entradas en el registro de eventos de NT que indican las solicitudes de datos de entrada rechazadas a los espacios de nombres que requieren cifrado.</span><span class="sxs-lookup"><span data-stu-id="29479-124">You can check the NT Event Log for entries indicating rejected inbound data requests to namespaces that require encryption.</span></span>

## <a name="related-topics"></a><span data-ttu-id="29479-125">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="29479-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="29479-126">Configuración de descriptores de seguridad de espacio</span><span class="sxs-lookup"><span data-stu-id="29479-126">Setting Namepace Security Descriptors</span></span>](setting-namespace-security-descriptors.md)
</dt> <dt>

[<span data-ttu-id="29479-127">**WbemAuthenticationLevelEnum**</span><span class="sxs-lookup"><span data-stu-id="29479-127">**WbemAuthenticationLevelEnum**</span></span>](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemauthenticationlevelenum)
</dt> <dt>

[<span data-ttu-id="29479-128">Protección de una conexión WMI remota</span><span class="sxs-lookup"><span data-stu-id="29479-128">Securing a Remote WMI Connection</span></span>](securing-a-remote-wmi-connection.md)
</dt> </dl>

 

 



