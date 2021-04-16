---
title: Compilación de MIDL
description: Compilación de MIDL
ms.assetid: 2797ee3b-82fd-4cb5-9e95-23b2f2a8f011
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e281fa66ec1b8f997dd58fc55a67c19a801d2d36
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/21/2020
ms.locfileid: "104488334"
---
# <a name="midl-compilation"></a><span data-ttu-id="3198b-103">Compilación de MIDL</span><span class="sxs-lookup"><span data-stu-id="3198b-103">MIDL Compilation</span></span>

<span data-ttu-id="3198b-104">Dado un archivo IDL, como [Example2. idl](anatomy-of-an-idl-file.md), que define una o más interfaces com y una biblioteca de tipos, el compilador de MIDL (Midl.exe) genera los archivos que se describen en la tabla siguiente como la salida predeterminada.</span><span class="sxs-lookup"><span data-stu-id="3198b-104">Given an IDL file, such as [Example2.idl](anatomy-of-an-idl-file.md), that defines one or more COM interfaces and a type library, the MIDL compiler (Midl.exe) generates the files described in the following table as the default output.</span></span>



| <span data-ttu-id="3198b-105">Nombre de archivo</span><span class="sxs-lookup"><span data-stu-id="3198b-105">Filename</span></span>                 | <span data-ttu-id="3198b-106">Descripción</span><span class="sxs-lookup"><span data-stu-id="3198b-106">Description</span></span>                                                                                                                                                                                           |
|--------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3198b-107">Example2. h</span><span class="sxs-lookup"><span data-stu-id="3198b-107">Example2.h</span></span><br/>    | <span data-ttu-id="3198b-108">El archivo de encabezado, que contiene definiciones de tipos y declaraciones de función para todas las interfaces definidas en el archivo IDL, así como declaraciones adelantadas para las rutinas a las que llama el código auxiliar.</span><span class="sxs-lookup"><span data-stu-id="3198b-108">The header file, containing type definitions and function declarations for all of the interfaces defined in the IDL file as well as forward declarations for routines that the stubs call.</span></span><br/> |
| <span data-ttu-id="3198b-109">Example2 \_ p. c</span><span class="sxs-lookup"><span data-stu-id="3198b-109">Example2\_p.c</span></span><br/> | <span data-ttu-id="3198b-110">El archivo de proxy/código auxiliar, que incluye los puntos de entrada suplentes tanto para los clientes como para los servidores.</span><span class="sxs-lookup"><span data-stu-id="3198b-110">The proxy/stub file, which includes the surrogate entry points both for clients and for servers.</span></span><br/>                                                                                           |
| <span data-ttu-id="3198b-111">Example2 \_ c</span><span class="sxs-lookup"><span data-stu-id="3198b-111">Example2\_i.c</span></span><br/> | <span data-ttu-id="3198b-112">El archivo de identificador de interfaz, que define el GUID para cada interfaz especificada en el archivo IDL.</span><span class="sxs-lookup"><span data-stu-id="3198b-112">The interface ID file, which defines the GUID for every interface specified in the IDL file.</span></span><br/>                                                                                               |
| <span data-ttu-id="3198b-113">Example2. tlb</span><span class="sxs-lookup"><span data-stu-id="3198b-113">Example2.tlb</span></span><br/>  | <span data-ttu-id="3198b-114">Archivo de documento compuesto que contiene información sobre tipos y objetos.</span><span class="sxs-lookup"><span data-stu-id="3198b-114">A compound document file that contains information about types and objects.</span></span><br/>                                                                                                                |
| <span data-ttu-id="3198b-115">Dlldata. c</span><span class="sxs-lookup"><span data-stu-id="3198b-115">Dlldata.c</span></span><br/>     | <span data-ttu-id="3198b-116">Contiene los datos que necesita para crear un archivo DLL de proxy/código auxiliar.</span><span class="sxs-lookup"><span data-stu-id="3198b-116">Contains the data you need to create a proxy/stub DLL.</span></span><br/>                                                                                                                                     |



 

<span data-ttu-id="3198b-117">Use el archivo de encabezado y todos los archivos. c para [crear un archivo dll de proxy](building-and-registering-a-proxy-dll.md) que pueda admitir la interfaz cuando lo usen las aplicaciones cliente y los servidores de objetos.</span><span class="sxs-lookup"><span data-stu-id="3198b-117">You use the header file and all of the .c files to [create a proxy DLL](building-and-registering-a-proxy-dll.md) that can support the interface when used both by client applications and by object servers.</span></span> <span data-ttu-id="3198b-118">El archivo de encabezado de interfaz (Example2. h) y el archivo de identificador de interfaz (Example2 \_ i. c) se usan al crear el archivo ejecutable para una aplicación cliente que utiliza la interfaz.</span><span class="sxs-lookup"><span data-stu-id="3198b-118">You use the interface header file (Example2.h) and the interface ID (Example2\_i.c) file when creating the executable file for a client application that uses the interface.</span></span> <span data-ttu-id="3198b-119">Puede optar por incluir el archivo de biblioteca de tipos como un recurso en el archivo EXE o DLL, o bien puede enviarlo como un archivo independiente.</span><span class="sxs-lookup"><span data-stu-id="3198b-119">You can choose to include the type library file as a resource in your EXE or DLL, or you can ship it as a separate file.</span></span>

## <a name="related-topics"></a><span data-ttu-id="3198b-120">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="3198b-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3198b-121">Archivos generados para una interfaz COM</span><span class="sxs-lookup"><span data-stu-id="3198b-121">Files Generated for a COM Interface</span></span>](/windows/desktop/Midl/files-generated-for-a-com-interface)
</dt> <dt>

[<span data-ttu-id="3198b-122">Opciones del compilador de MIDL</span><span class="sxs-lookup"><span data-stu-id="3198b-122">MIDL Compiler Options</span></span>](midl-compiler-options.md)
</dt> </dl>

 

