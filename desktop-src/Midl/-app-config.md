---
title: modificador/app_config
description: El \_ modificador/App config selecciona el modo de configuración de la aplicación, que permite usar algunas palabras clave ACF en el archivo IDL. Con este modificador de compilador de MIDL, puede omitir ACF y especificar una interfaz en un solo archivo IDL.
ms.assetid: 8d12a0ed-7eaa-4ebc-a961-b726aefefadc
keywords:
- /app_config modificador MIDL
topic_type:
- apiref
api_name:
- /app_config
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 717d5234bd419fec7107a6d983ece026b4558935
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/25/2019
ms.locfileid: "104419655"
---
# <a name="app_config-switch"></a><span data-ttu-id="5e596-105">\_modificador de configuración de/App</span><span class="sxs-lookup"><span data-stu-id="5e596-105">/app\_config switch</span></span>

<span data-ttu-id="5e596-106">El modificador **/App \_ config** selecciona el modo de configuración de la aplicación, que permite usar algunas palabras clave ACF en el archivo IDL.</span><span class="sxs-lookup"><span data-stu-id="5e596-106">The **/app\_config** switch selects application-configuration mode, which allows you to use some ACF keywords in the IDL file.</span></span> <span data-ttu-id="5e596-107">Con este modificador de compilador de MIDL, puede omitir ACF y especificar una interfaz en un solo archivo IDL.</span><span class="sxs-lookup"><span data-stu-id="5e596-107">With this MIDL compiler switch, you can omit the ACF and specify an interface in a single IDL file.</span></span>

``` syntax
midl /app_config
```

## <a name="switch-options"></a><span data-ttu-id="5e596-108">Opciones de conmutador</span><span class="sxs-lookup"><span data-stu-id="5e596-108">Switch Options</span></span>

<span data-ttu-id="5e596-109">Este modificador no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="5e596-109">This switch has no parameters.</span></span>

## <a name="remarks"></a><span data-ttu-id="5e596-110">Observaciones</span><span class="sxs-lookup"><span data-stu-id="5e596-110">Remarks</span></span>

<span data-ttu-id="5e596-111">Microsoft RPC admite el uso de los siguientes atributos ACF en el archivo IDL:</span><span class="sxs-lookup"><span data-stu-id="5e596-111">Microsoft RPC supports the use of the following ACF attributes in the IDL file:</span></span>

-   <span data-ttu-id="5e596-112">\_Identificador implícito</span><span class="sxs-lookup"><span data-stu-id="5e596-112">Implicit\_handle</span></span>
-   <span data-ttu-id="5e596-113">\_Identificador automático</span><span class="sxs-lookup"><span data-stu-id="5e596-113">Auto\_handle</span></span>
-   <span data-ttu-id="5e596-114">\_Identificador explícito</span><span class="sxs-lookup"><span data-stu-id="5e596-114">Explicit\_handle</span></span>

<span data-ttu-id="5e596-115">Las versiones futuras de Microsoft RPC pueden admitir el uso de otros atributos ACF en el archivo IDL.</span><span class="sxs-lookup"><span data-stu-id="5e596-115">Future releases of Microsoft RPC may support the use of other ACF attributes in the IDL file.</span></span> <span data-ttu-id="5e596-116">La opción de **\_ configuración/App** representa una extensión de Microsoft para la especificación de OSF-DCE y, como tal, es mutuamente excluyente con la opción [**/OSF**](-osf.md) .</span><span class="sxs-lookup"><span data-stu-id="5e596-116">The **/app\_config** option represents a Microsoft extension to the OSF-DCE specification and, as such, is mutually exclusive with the [**/osf**](-osf.md) option.</span></span>

<span data-ttu-id="5e596-117">Para obtener más información relacionada con el modificador **/App \_ config** , vea archivo de configuración de la [aplicación (ACF)](application-configuration-file-acf-.md) y [archivo de definición de interfaz (IDL)](interface-definition-idl-file.md).</span><span class="sxs-lookup"><span data-stu-id="5e596-117">For more information related to the **/app\_config** switch, see [Application Configuration File (ACF)](application-configuration-file-acf-.md) and [Interface Definition (IDL) File](interface-definition-idl-file.md).</span></span>

## <a name="examples"></a><span data-ttu-id="5e596-118">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="5e596-118">Examples</span></span>

<span data-ttu-id="5e596-119">**MIDL/APP \_ config nombreDeArchivo. idl**</span><span class="sxs-lookup"><span data-stu-id="5e596-119">**midl /app\_config filename.idl**</span></span>

## <a name="see-also"></a><span data-ttu-id="5e596-120">Vea también</span><span class="sxs-lookup"><span data-stu-id="5e596-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5e596-121">Sintaxis de línea de comandos de MIDL general</span><span class="sxs-lookup"><span data-stu-id="5e596-121">General MIDL Command-line Syntax</span></span>](general-midl-command-line-syntax.md)
</dt> </dl>

 

 




