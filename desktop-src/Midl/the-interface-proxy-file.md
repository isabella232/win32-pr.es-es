---
title: El archivo de proxy de interfaz
description: El archivo de proxy de interfaz (U \_ p. c) es un archivo de c que contiene rutinas equivalentes a las de los archivos de código auxiliar de cliente y de código auxiliar de servidor de una interfaz de objeto (com).
ms.assetid: f85f7384-a590-4146-9705-2e87f1a0a87a
keywords:
- MIDL y COM MIDL, interfaces y archivos proxy
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7be52b3561af03df0375212d729f64f41e3cdd7b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103994415"
---
# <a name="the-interface-proxy-file"></a><span data-ttu-id="66660-104">El archivo de proxy de interfaz</span><span class="sxs-lookup"><span data-stu-id="66660-104">The Interface Proxy File</span></span>

<span data-ttu-id="66660-105">El archivo de proxy de interfaz (U \_ p. c) es un archivo de c que contiene rutinas equivalentes a las de los archivos de código auxiliar de cliente y de código auxiliar de servidor de una interfaz de objeto (com).</span><span class="sxs-lookup"><span data-stu-id="66660-105">The interface proxy file (U\_p.c) is a C file that contains routines equivalent to those in the client stub and server stub files of an object (COM) interface.</span></span> <span data-ttu-id="66660-106">Este archivo contiene implementaciones de las rutinas suplentes para el cliente y el servidor en el modo en línea del compilador o datos equivalentes y thunks en los modos interpretados, así como otros datos de adherencia COM adecuados, como el proxy y las tablas auxiliares de código auxiliar.</span><span class="sxs-lookup"><span data-stu-id="66660-106">This file contains implementations of the surrogate routines for client and server in the inline mode of the compiler or equivalent data and thunks in the interpreted modes, as well as other appropriate COM glue data, such as the proxy and stub Vtables.</span></span>

<span data-ttu-id="66660-107">El archivo de proxy de interfaz incluye las rutinas y los datos auxiliares solo para los métodos de las interfaces definidas en el archivo IDL actual.</span><span class="sxs-lookup"><span data-stu-id="66660-107">The interface proxy file includes the supporting routines and data only for methods of the interfaces defined in the current IDL file.</span></span> <span data-ttu-id="66660-108">Para aclarar este comportamiento, se usa un ejemplo extendido en esta sección.</span><span class="sxs-lookup"><span data-stu-id="66660-108">To clarify this behavior, an extended example is used throughout this section.</span></span> <span data-ttu-id="66660-109">Al compilar un archivo IDL con una interfaz como IFaceB que se hereda de IFaceA, se generan las rutinas y los datos auxiliares relacionados con IFaceB en el archivo proxy actual, mientras que la interfaz base IFaceA los datos y rutinas auxiliares relacionados se encuentran en el proxy generado a partir del archivo IDL que contiene la definición de IFaceA.</span><span class="sxs-lookup"><span data-stu-id="66660-109">When compiling an IDL file with an interface such as IFaceB that inherits from IFaceA, IFaceB related auxiliary data and routines are generated to the current proxy file, while the base interface IFaceA related auxiliary data and routines are found in the proxy generated from the IDL file containing the IFaceA definition.</span></span> <span data-ttu-id="66660-110">El compilador genera todos los datos necesarios para identificar los suplentes de la interfaz base y delegarlos cuando sea necesario para admitir los métodos de IFaceA usados a través de la interfaz IFaceB.</span><span class="sxs-lookup"><span data-stu-id="66660-110">The compiler generates all data necessary to identify the surrogates of the base interface, and to delegate to them when needed to support the IFaceA methods used through IFaceB interface.</span></span>

<span data-ttu-id="66660-111">Para cada método de una interfaz en el archivo IDL actual, el archivo del proxy contiene los dos métodos suplentes siguientes cuando se compilan en el modo mixto ([/os](-os.md)) y los datos de intérprete equivalentes cuando se compilan en el modo de intérprete ([/OI](-oi.md)).</span><span class="sxs-lookup"><span data-stu-id="66660-111">For every method in an interface in the current IDL file, the proxy file contains the following two surrogate methods when compiled in the mixed mode ([/Os](-os.md)), and equivalent interpreter data when compiled in the interpreter mode ([/Oi](-oi.md)).</span></span>

-   <span data-ttu-id="66660-112">El suplente del lado cliente, como el \_ proxy del método IFaceB \_ en este ejemplo.</span><span class="sxs-lookup"><span data-stu-id="66660-112">The client-side surrogate, such as IFaceB\_Method\_Proxy in this example.</span></span>

    <span data-ttu-id="66660-113">Este suplente del lado cliente es el punto de entrada virtual al que el cliente, por ejemplo, IFaceB:: Method, envía.</span><span class="sxs-lookup"><span data-stu-id="66660-113">This client-side surrogate is the virtual entry point to which the client, for example IFaceB::Method, dispatches.</span></span> <span data-ttu-id="66660-114">Calcula las referencias de los argumentos de entrada en un formato de transmisión, transmite los argumentos de cálculo de referencias junto con información que identifica la interfaz y la operación y, a continuación, anula las referencias del valor devuelto y de los argumentos de salida cuando se devuelve la operación invocada.</span><span class="sxs-lookup"><span data-stu-id="66660-114">It marshals the input arguments into a transmittable form, transmits the marshaled arguments along with information that identifies the interface and the operation, and then unmarshals the return value and any output arguments when the invoked operation returns.</span></span>

-   <span data-ttu-id="66660-115">El suplente del lado servidor, por ejemplo, el \_ código auxiliar del método IFaceB \_ .</span><span class="sxs-lookup"><span data-stu-id="66660-115">The server-side surrogate, for example, IFaceB\_Method\_Stub .</span></span>

    <span data-ttu-id="66660-116">Este suplente del lado servidor es el punto de entrada virtual en el que se envía el tiempo de ejecución subyacente en el servidor para emular el cliente.</span><span class="sxs-lookup"><span data-stu-id="66660-116">This server-side surrogate is the virtual entry point that the underlying runtime dispatches to at the server to emulate the client.</span></span> <span data-ttu-id="66660-117">Anula las referencias de los argumentos de entrada para replicar los datos de cliente, invoca la implementación del servidor de la función de interfaz y, a continuación, calcula las referencias y transmite el valor devuelto y los argumentos de salida al lado cliente.</span><span class="sxs-lookup"><span data-stu-id="66660-117">It unmarshals the input arguments to replicate the client data, invokes the server's implementation of the interface function, and then marshals and transmits the return value and any output arguments back to the client side.</span></span>

<span data-ttu-id="66660-118">El nombre predeterminado de un archivo proxy generado a partir de un archivo. idl es el archivo \_ p. c. Use el modificador del compilador MIDL de [**/proxy**](-proxy.md) para reemplazar el nombre predeterminado del archivo proxy de interfaz.</span><span class="sxs-lookup"><span data-stu-id="66660-118">The default name for a proxy file generated from a file.idl is file\_p.c.Use the [**/proxy**](-proxy.md) MIDL compiler switch to override the default name of the interface proxy file.</span></span> <span data-ttu-id="66660-119">Los modificadores [**/env**](-env.md) y [**/out**](-out.md) afectan a este archivo.</span><span class="sxs-lookup"><span data-stu-id="66660-119">The [**/env**](-env.md) and [**/out**](-out.md) switches affect this file.</span></span>

 

 




