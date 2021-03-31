---
title: LocalServer32
description: Especifica la ruta de acceso completa a una aplicación de servidor local de 32 bits.
ms.assetid: 5d922230-f53d-4bf9-be50-c8c00f45b7a8
keywords:
- Clave del registro LocalServer32 COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4fd068f51f33b6c283384198c0206bc9c3b6357f
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/21/2020
ms.locfileid: "104533550"
---
# <a name="localserver32"></a><span data-ttu-id="d2308-104">LocalServer32</span><span class="sxs-lookup"><span data-stu-id="d2308-104">LocalServer32</span></span>

<span data-ttu-id="d2308-105">Especifica la ruta de acceso completa a una aplicación de servidor local de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="d2308-105">Specifies the full path to a 32-bit local server application.</span></span>

## <a name="registry-entry"></a><span data-ttu-id="d2308-106">Entrada del Registro</span><span class="sxs-lookup"><span data-stu-id="d2308-106">Registry Entry</span></span>

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\CLSID
   {CLSID}
      LocalServer32
         (Default) = path
         ServerExecutable = path
```

## <a name="remarks"></a><span data-ttu-id="d2308-107">Observaciones</span><span class="sxs-lookup"><span data-stu-id="d2308-107">Remarks</span></span>

<span data-ttu-id="d2308-108">El valor **ServerExecutable** , que es de tipo **reg \_ SZ** y se admite a partir de Windows Server 2003, funciona junto con la subclave **LocalServer32** para evitar ambigüedades al utilizar la función [**CreateProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa) .</span><span class="sxs-lookup"><span data-stu-id="d2308-108">The **ServerExecutable** value, which is of type **REG\_SZ** and is supported starting with Windows Server 2003, works in conjunction with the **LocalServer32** subkey to prevent any ambiguity when using the [**CreateProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa) function.</span></span> <span data-ttu-id="d2308-109">**LocalServer32** especifica la ubicación de la aplicación de servidor com que se va a iniciar y esta información se pasa como el primer parámetro *lpApplicationName* para **CreateProcess**.</span><span class="sxs-lookup"><span data-stu-id="d2308-109">**LocalServer32** specifies the location of the COM server application to launch, and this information is passed as the first parameter *lpApplicationName* for **CreateProcess**.</span></span> <span data-ttu-id="d2308-110">Dependiendo de la implementación de **CreateProcess**, esta información puede ser ambigua.</span><span class="sxs-lookup"><span data-stu-id="d2308-110">Depending on the implementation of **CreateProcess**, this information might be ambiguous.</span></span> <span data-ttu-id="d2308-111">Por esta razón, si se especifica **ServerExecutable** , com pasa el valor con nombre **ServerExecutable** al parámetro *lpApplicationName* de **CreateProcess**.</span><span class="sxs-lookup"><span data-stu-id="d2308-111">For this reason, if **ServerExecutable** is specified, COM passes the **ServerExecutable** named value to the *lpApplicationName* parameter of **CreateProcess**.</span></span> <span data-ttu-id="d2308-112">Si no se especifica **ServerExecutable** , com pasa **null** como el valor para el primer parámetro de **CreateProcess**.</span><span class="sxs-lookup"><span data-stu-id="d2308-112">If **ServerExecutable** is not specified, COM passes **NULL** as the value for the first parameter of **CreateProcess**.</span></span>

<span data-ttu-id="d2308-113">Para ayudar a proporcionar seguridad del sistema, utilice cadenas entre comillas en la ruta de acceso para indicar dónde finaliza el nombre del archivo ejecutable y los argumentos comienzan.</span><span class="sxs-lookup"><span data-stu-id="d2308-113">To help provide system security, use quoted strings in the path to indicate where the executable filename ends and the arguments begin.</span></span> <span data-ttu-id="d2308-114">Por ejemplo, en lugar de especificar la siguiente ruta de acceso como la entrada de **LocalServer32** :</span><span class="sxs-lookup"><span data-stu-id="d2308-114">For example, instead of specifying the following path as the **LocalServer32** entry:</span></span>

<span data-ttu-id="d2308-115">"C: archivos de la \\ compañía de archivos de programa \\ \\Application.exe parám1 param2"</span><span class="sxs-lookup"><span data-stu-id="d2308-115">"C:\\Program Files\\Company Files\\Application.exe param1 param2"</span></span>

<span data-ttu-id="d2308-116">Especifique la ruta de acceso con la siguiente sintaxis:</span><span class="sxs-lookup"><span data-stu-id="d2308-116">specify the path using the following syntax:</span></span>

<span data-ttu-id="d2308-117">" \\ C: archivos de la \\ compañía de archivos de programa \\ \\Application.exe\\ " parám1 parám2 "</span><span class="sxs-lookup"><span data-stu-id="d2308-117">"\\"C:\\Program Files\\Company Files\\Application.exe\\" param1 param2"</span></span>

<span data-ttu-id="d2308-118">COM anexa la marca "-Embedding" a la cadena, por lo que la aplicación que usa marcas debe analizar toda la cadena y comprobar la marca-Embedding.</span><span class="sxs-lookup"><span data-stu-id="d2308-118">COM appends the "-Embedding" flag to the string, so the application that uses flags needs to parse the whole string and check for the -Embedding flag.</span></span>

<span data-ttu-id="d2308-119">Cuando COM inicia un servidor local de 32 bits, el servidor debe registrar un objeto de clase dentro de un tiempo transcurrido establecido por el usuario.</span><span class="sxs-lookup"><span data-stu-id="d2308-119">When COM starts a 32-bit local server, the server must register a class object within an elapsed time set by the user.</span></span> <span data-ttu-id="d2308-120">De forma predeterminada, el valor de tiempo transcurrido debe ser de al menos 5 minutos, en milisegundos, pero no puede superar el número de milisegundos en 30 días.</span><span class="sxs-lookup"><span data-stu-id="d2308-120">By default, the elapsed time value must be at least 5 minutes, in milliseconds, but cannot exceed the number of milliseconds in 30 days.</span></span> <span data-ttu-id="d2308-121">Normalmente, las aplicaciones no deben establecer este valor, que se encuentra en la entrada **HKEY \_ local \_ Machine \\ software \\ Microsoft \\ COM2 \\ ServerStartElapsedTime** .</span><span class="sxs-lookup"><span data-stu-id="d2308-121">Applications typically should not set this value, which is in the **HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\COM2\\ServerStartElapsedTime** entry.</span></span>

<span data-ttu-id="d2308-122">Las entradas necesarias para los servidores locales de 32 bits son [**InprocHandler32**](inprochandler32.md), [**LocalServer**](localserver.md), **LocalServer32** e [**inserciones**](insertable.md).</span><span class="sxs-lookup"><span data-stu-id="d2308-122">The required entries for 32-bit local servers are [**InprocHandler32**](inprochandler32.md), [**LocalServer**](localserver.md), **LocalServer32**, and [**Insertable**](insertable.md).</span></span>

<span data-ttu-id="d2308-123">Si un contenedor está buscando en el registro un servidor local, un servidor local de 32 bits tiene prioridad sobre un servidor local de 16 bits.</span><span class="sxs-lookup"><span data-stu-id="d2308-123">If a container is searching the registry for a local server, a 32-bit local server has priority over a 16-bit local server.</span></span>

<span data-ttu-id="d2308-124">Si va a implementar clases como servicios, debe tener en cuenta que se usa el valor con nombre [**LocalService**](localservice.md) en preferencia a la clave **LocalServer32** para la activación local y remota Requestsâ € "Si **LocalService** existe y hace referencia a un servicio válido, se omite la clave **LocalServer32** .</span><span class="sxs-lookup"><span data-stu-id="d2308-124">If you are implementing classes as services, you should be aware that the [**LocalService**](localservice.md) named value is used in preference to the **LocalServer32** key for local and remote activation requestsâ€”if **LocalService** exists and refers to a valid service, the **LocalServer32** key is ignored.</span></span>

## <a name="related-topics"></a><span data-ttu-id="d2308-125">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="d2308-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d2308-126">**LocalServer**</span><span class="sxs-lookup"><span data-stu-id="d2308-126">**LocalServer**</span></span>](localserver.md)
</dt> <dt>

[<span data-ttu-id="d2308-127">**LocalService (Servicio local)**</span><span class="sxs-lookup"><span data-stu-id="d2308-127">**LocalService**</span></span>](localservice.md)
</dt> </dl>

 

 