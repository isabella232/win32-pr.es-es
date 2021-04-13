---
title: Destinar códigos auxiliares para plataformas específicas de 32 bits o 64 bits
description: Algunas de las características de Microsoft RPC y los compiladores MIDL 3,0 y versiones posteriores son específicas de la plataforma.
ms.assetid: bb1bee56-7f39-406c-bdbf-b73bda568247
keywords:
- '32: plataformas de bits MIDL'
- '64: plataformas de bits MIDL'
- código de la auxiliar MIDL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 526265a60f8b2ef2f31d19d0356d4ec3a3ae8c8f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104357448"
---
# <a name="targeting-stubs-for-specific-32-bit-or-64-bit-platforms"></a><span data-ttu-id="b6a51-106">Destinar códigos auxiliares para plataformas específicas de 32 bits o 64 bits</span><span class="sxs-lookup"><span data-stu-id="b6a51-106">Targeting Stubs for Specific 32-bit or 64-bit Platforms</span></span>

<span data-ttu-id="b6a51-107">Algunas de las características de Microsoft RPC y los compiladores MIDL 3,0 y versiones posteriores son específicas de la plataforma.</span><span class="sxs-lookup"><span data-stu-id="b6a51-107">Some of the features of Microsoft RPC and the MIDL 3.0 and later compilers are platform-specific.</span></span>

<span data-ttu-id="b6a51-108">Como medida de precaución, los compiladores MIDL 3,0 y versiones posteriores generan protecciones que facilitan la comprobación de compatibilidad durante la fase de compilación de C.</span><span class="sxs-lookup"><span data-stu-id="b6a51-108">As a precaution, the MIDL 3.0 and later compilers generate guards that facilitate compatibility checking during the C-compilation phase.</span></span> <span data-ttu-id="b6a51-109">MIDL genera dos tipos de protecciones: una protección dependiente de la plataforma (32 bits frente a 64 bits) y una protección dependiente de la versión (dependencia del conjunto de características).</span><span class="sxs-lookup"><span data-stu-id="b6a51-109">MIDL generates two types of guards: a platform-dependent guard (32-bit versus 64-bit) and a release-dependent guard (feature set dependency).</span></span> <span data-ttu-id="b6a51-110">Por ejemplo, MIDL genera la siguiente protección para evitar la compilación de C de un código auxiliar de 32 bits para otras plataformas:</span><span class="sxs-lookup"><span data-stu-id="b6a51-110">For example, MIDL generates the following guard to prevent C-compiling of a 32-bit stub for other platforms:</span></span>

``` syntax
#if !defined(__RPC_WIN32__)
#error  Invalid build platform for this stub.
#endif
```

<span data-ttu-id="b6a51-111">La protección dependiente de la versión se desencadena mediante un conjunto de características que se encuentran en los archivos IDL procesados y el modificador [**/target**](-target.md) .</span><span class="sxs-lookup"><span data-stu-id="b6a51-111">The release-dependent guard is triggered by a set of features found in the processed IDL file(s) and by the [**/target**](-target.md) switch.</span></span> <span data-ttu-id="b6a51-112">Por ejemplo, si la interfaz utiliza características admitidas solo en Windows 2000 o posterior, MIDL genera una protección con el destino \_ es \_ NT50 \_ o \_ una macro posterior.</span><span class="sxs-lookup"><span data-stu-id="b6a51-112">For example, if the interface uses features supported only on WindowsÂ 2000 or later, MIDL generates a guard with the TARGET\_IS\_NT50\_OR\_LATER macro.</span></span>

<span data-ttu-id="b6a51-113">Las macros Guard, definidas en Rpcndr. h, dependen de la configuración de WINVER y \_ Win32 \_ WinNT y se evalúan mediante el compilador de C/C++.</span><span class="sxs-lookup"><span data-stu-id="b6a51-113">The guard macros, defined in Rpcndr.h, depend on the setting of WINVER and \_WIN32\_WINNT and are evaluated by the C/C++ compiler.</span></span>

<span data-ttu-id="b6a51-114">Si, en tiempo de compilación de C, recibe un mensaje de error que indica que necesita una plataforma específica para ejecutar un código auxiliar, primero debe comprobar para asegurarse de que no ha usado una característica que no está disponible en esta plataforma.</span><span class="sxs-lookup"><span data-stu-id="b6a51-114">If, at C-compile time, you get an error message indicating that you need a specific platform to run a stub, first check to make sure you have not used a feature that is not available on this platform.</span></span> <span data-ttu-id="b6a51-115">Las características que desencadenan una protección determinada se muestran en el cuerpo de la protección.</span><span class="sxs-lookup"><span data-stu-id="b6a51-115">The features triggering a particular guard are listed in the body of the guard.</span></span> <span data-ttu-id="b6a51-116">En el ejemplo anterior, el modificador de compilador-Oicf activó la protección.</span><span class="sxs-lookup"><span data-stu-id="b6a51-116">In the previous example, the -Oicf compiler switch triggered the guard.</span></span> <span data-ttu-id="b6a51-117">Entre las características importantes de este tipo se incluyen el modificador [**/Robust**](-robust.md) y el \[ atributo [**async**](async.md) \] disponible en Windows 2000 y versiones posteriores, el constructor de tipo de [**canalización**](pipe.md) , la opción del compilador/OIF y los atributos Marshal y serialización del \[ [**usuario \_**](user-marshal.md) \] \[ [**\_**](wire-marshal.md) \] .</span><span class="sxs-lookup"><span data-stu-id="b6a51-117">Notable features of this kind include the [**/robust**](-robust.md) switch and the \[[**async**](async.md)\] attribute available on WindowsÂ 2000 and later, the [**pipe**](pipe.md) type constructor, the /Oif compiler option, and the \[[**user\_marshal**](user-marshal.md)\] and \[[**wire\_marshal**](wire-marshal.md)\] attributes.</span></span> <span data-ttu-id="b6a51-118">Los códigos auxiliares que usan estas características no se ejecutarán en sistemas anteriores.</span><span class="sxs-lookup"><span data-stu-id="b6a51-118">Stubs using these features will not run on earlier systems.</span></span>

<span data-ttu-id="b6a51-119">Si sabe que la plataforma de destino es correcta para las características que está usando y sigue recibiendo un error, puede que tenga que establecer las variables de entorno de forma adecuada.</span><span class="sxs-lookup"><span data-stu-id="b6a51-119">If you know that your target platform is correct for the features you are using and still receive an error, you may need to set the environment variables appropriately.</span></span>

<span data-ttu-id="b6a51-120">**Para compilar para Windows 2000 o versiones posteriores**</span><span class="sxs-lookup"><span data-stu-id="b6a51-120">**To build for WindowsÂ 2000 or later releases**</span></span>

-   <span data-ttu-id="b6a51-121">Agregue esta línea al archivo Make:</span><span class="sxs-lookup"><span data-stu-id="b6a51-121">Add this line to your makefile:</span></span>

    ``` syntax
    CFLAGS = $(CFLAGS) -D_WIN32_WINNT=0x500
    ```

## <a name="related-topics"></a><span data-ttu-id="b6a51-122">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="b6a51-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b6a51-123">**/Target**</span><span class="sxs-lookup"><span data-stu-id="b6a51-123">**/target**</span></span>](-target.md)
</dt> <dt>

[<span data-ttu-id="b6a51-124">**/Robust**</span><span class="sxs-lookup"><span data-stu-id="b6a51-124">**/robust**</span></span>](-robust.md)
</dt> <dt>

[<span data-ttu-id="b6a51-125">**async**</span><span class="sxs-lookup"><span data-stu-id="b6a51-125">**async**</span></span>](async.md)
</dt> <dt>

[<span data-ttu-id="b6a51-126">**\_UUID asincrónico**</span><span class="sxs-lookup"><span data-stu-id="b6a51-126">**async\_uuid**</span></span>](async-uuid.md)
</dt> <dt>

[<span data-ttu-id="b6a51-127">**/OI**</span><span class="sxs-lookup"><span data-stu-id="b6a51-127">**/Oi**</span></span>](-oi.md)
</dt> <dt>

[<span data-ttu-id="b6a51-128">**codo**</span><span class="sxs-lookup"><span data-stu-id="b6a51-128">**pipe**</span></span>](pipe.md)
</dt> <dt>

[<span data-ttu-id="b6a51-129">**\_serialización de cable**</span><span class="sxs-lookup"><span data-stu-id="b6a51-129">**wire\_marshal**</span></span>](wire-marshal.md)
</dt> <dt>

[<span data-ttu-id="b6a51-130">**\_serialización de usuario**</span><span class="sxs-lookup"><span data-stu-id="b6a51-130">**user\_marshal**</span></span>](user-marshal.md)
</dt> <dt>

[<span data-ttu-id="b6a51-131">Serialización de tipos de datos OLE</span><span class="sxs-lookup"><span data-stu-id="b6a51-131">Marshaling OLE Data Types</span></span>](marshaling-ole-data-types.md)
</dt> </dl>

 

 




