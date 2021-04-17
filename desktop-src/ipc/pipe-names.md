---
description: Cada canalización con nombre tiene un nombre único que la distingue de otras canalizaciones con nombre en la lista sistemas de objetos con nombre. Un servidor de canalización especifica un nombre para la canalización cuando llama a la función CreateNamedPipe para crear una o varias instancias de una canalización con nombre.
ms.assetid: 8f7e717a-648b-421e-ab79-a4abbae670be
title: Nombres de canalización
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e470a09fa4cfe1b2f259ca3fd5b53f79045787fb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105688392"
---
# <a name="pipe-names"></a><span data-ttu-id="47f32-104">Nombres de canalización</span><span class="sxs-lookup"><span data-stu-id="47f32-104">Pipe Names</span></span>

<span data-ttu-id="47f32-105">Cada canalización con nombre tiene un nombre único que la distingue de otras canalizaciones con nombre en la lista de objetos con nombre del sistema.</span><span class="sxs-lookup"><span data-stu-id="47f32-105">Each named pipe has a unique name that distinguishes it from other named pipes in the system's list of named objects.</span></span> <span data-ttu-id="47f32-106">Un servidor de canalización especifica un nombre para la canalización cuando llama a la función [**CreateNamedPipe**](/windows/desktop/api/Winbase/nf-winbase-createnamedpipea) para crear una o varias instancias de una canalización con nombre.</span><span class="sxs-lookup"><span data-stu-id="47f32-106">A pipe server specifies a name for the pipe when it calls the [**CreateNamedPipe**](/windows/desktop/api/Winbase/nf-winbase-createnamedpipea) function to create one or more instances of a named pipe.</span></span> <span data-ttu-id="47f32-107">Los clientes de canalización especifican el nombre de la canalización cuando llaman a la función [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) o [**CallNamedPipe**](/windows/desktop/api/Winbase/nf-winbase-callnamedpipea) para conectarse a una instancia de la canalización con nombre.</span><span class="sxs-lookup"><span data-stu-id="47f32-107">Pipe clients specify the pipe name when they call the [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) or [**CallNamedPipe**](/windows/desktop/api/Winbase/nf-winbase-callnamedpipea) function to connect to an instance of the named pipe.</span></span>

<span data-ttu-id="47f32-108">Utilice el siguiente formato al especificar el nombre de una canalización en la función [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea), [**WaitNamedPipe**](/windows/desktop/api/Winbase/nf-winbase-waitnamedpipea)o [**CallNamedPipe**](/windows/desktop/api/Winbase/nf-winbase-callnamedpipea) :</span><span class="sxs-lookup"><span data-stu-id="47f32-108">Use the following form when specifying the name of a pipe in the [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea), [**WaitNamedPipe**](/windows/desktop/api/Winbase/nf-winbase-waitnamedpipea), or [**CallNamedPipe**](/windows/desktop/api/Winbase/nf-winbase-callnamedpipea) function:</span></span>

<span data-ttu-id="47f32-109">\\\\*NombreDeServidor* \\ canalización \\ *PipeName*</span><span class="sxs-lookup"><span data-stu-id="47f32-109">\\\\*ServerName*\\pipe\\*PipeName*</span></span>

<span data-ttu-id="47f32-110">donde *ServerName* es el nombre de un equipo remoto o un punto, para especificar el equipo local.</span><span class="sxs-lookup"><span data-stu-id="47f32-110">where *ServerName* is either the name of a remote computer or a period, to specify the local computer.</span></span> <span data-ttu-id="47f32-111">La cadena de nombre de canalización especificada por *PipeName* puede incluir cualquier carácter que no sea una barra diagonal inversa, incluidos números y caracteres especiales.</span><span class="sxs-lookup"><span data-stu-id="47f32-111">The pipe name string specified by *PipeName* can include any character other than a backslash, including numbers and special characters.</span></span> <span data-ttu-id="47f32-112">Toda la cadena de nombre de canalización puede tener una longitud de hasta 256 caracteres.</span><span class="sxs-lookup"><span data-stu-id="47f32-112">The entire pipe name string can be up to 256 characters long.</span></span> <span data-ttu-id="47f32-113">Los nombres de canalización no distinguen mayúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="47f32-113">Pipe names are not case-sensitive.</span></span>

<span data-ttu-id="47f32-114">El servidor de canalización no puede crear una canalización en otro equipo, por lo que [**CreateNamedPipe**](/windows/desktop/api/Winbase/nf-winbase-createnamedpipea) debe usar un punto para el nombre del servidor, tal y como se muestra en el ejemplo siguiente.</span><span class="sxs-lookup"><span data-stu-id="47f32-114">The pipe server cannot create a pipe on another computer, so [**CreateNamedPipe**](/windows/desktop/api/Winbase/nf-winbase-createnamedpipea) must use a period for the server name, as shown in the following example.</span></span>

<span data-ttu-id="47f32-115">\\\\.\\ canalización \\ *PipeName*</span><span class="sxs-lookup"><span data-stu-id="47f32-115">\\\\.\\pipe\\*PipeName*</span></span>

<span data-ttu-id="47f32-116">Un servidor de canalización puede proporcionar el nombre de la canalización a sus clientes de canalización para que puedan conectarse a la canalización.</span><span class="sxs-lookup"><span data-stu-id="47f32-116">A pipe server can provide the pipe name to its pipe clients, so they can connect to the pipe.</span></span> <span data-ttu-id="47f32-117">El cliente de canalización detecta el nombre de la canalización desde algún origen persistente, como una entrada del registro, un archivo u otra aplicación.</span><span class="sxs-lookup"><span data-stu-id="47f32-117">The pipe client discovers the pipe name from some persistent source, such as a registry entry, a file, or another application.</span></span> <span data-ttu-id="47f32-118">De lo contrario, los clientes deben conocer el nombre de la canalización en tiempo de compilación.</span><span class="sxs-lookup"><span data-stu-id="47f32-118">Otherwise, the clients must know the pipe name at compile time.</span></span>

 

 
