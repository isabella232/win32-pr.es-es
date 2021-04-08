---
description: Asignación de nombres a los buzones y colocación de mensajes en los buzones.
ms.assetid: 1ef522a4-9786-427c-a18a-ae1f0a05cc50
title: Nombres de buzón de correo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bf03718a7e603fe891e00d82c2b0b06fab63f8f9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103808414"
---
# <a name="mailslot-names"></a><span data-ttu-id="0679b-103">Nombres de buzón de correo</span><span class="sxs-lookup"><span data-stu-id="0679b-103">Mailslot Names</span></span>

<span data-ttu-id="0679b-104">Cuando un proceso crea un buzón de correo, el nombre del buzón de correo debe tener el formato siguiente.</span><span class="sxs-lookup"><span data-stu-id="0679b-104">When a process creates a mailslot, the mailslot name must have the following form.</span></span>

<span data-ttu-id="0679b-105">\\\\.\\ nombre de \\ \[ *ruta de acceso* \\ \]  de buzón</span><span class="sxs-lookup"><span data-stu-id="0679b-105">\\\\.\\mailslot\\\[*path*\\\]*name*</span></span>

<span data-ttu-id="0679b-106">Un nombre de buzón de correo requiere los siguientes elementos: dos barras diagonales inversas para comenzar el nombre, un punto, una barra diagonal inversa después del punto, la palabra "buzón de correo" y una barra diagonal inversa final.</span><span class="sxs-lookup"><span data-stu-id="0679b-106">A mailslot name requires the following elements: two backslashes to begin the name, a period, a backslash following the period, the word "mailslot", and a trailing backslash.</span></span> <span data-ttu-id="0679b-107">Los nombres no distinguen mayúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="0679b-107">Names are not case sensitive.</span></span> <span data-ttu-id="0679b-108">Un nombre de buzón de correo puede ir precedido de un trazado que consta de los nombres de uno o varios directorios, separados por barras diagonales inversas.</span><span class="sxs-lookup"><span data-stu-id="0679b-108">A mailslot name can be preceded by a path consisting of the names of one or more directories, separated by backslashes.</span></span> <span data-ttu-id="0679b-109">Por ejemplo, si un usuario espera mensajes en el asunto de los impuestos de Bob, Ana y Sue, la aplicación de buzón de correo del usuario podría permitir al usuario crear buzones de correo individuales para cada remitente, como se muestra aquí:</span><span class="sxs-lookup"><span data-stu-id="0679b-109">For example, if a user expects messages on the subject of taxes from Bob, Pete, and Sue, the user's mailslot application might allow the user to create individual mailslots for each sender, as shown here:</span></span><dl> <span data-ttu-id="0679b-110">\\\\.\\ \\comentarios de \\ bobs de impuestos de buzón de correo \_</span><span class="sxs-lookup"><span data-stu-id="0679b-110">\\\\.\\mailslot\\taxes\\bobs\_comments</span></span>  
<span data-ttu-id="0679b-111">\\\\.\\ Comentarios de los Pedro de los impuestos de buzón de correo \\ \\ \_</span><span class="sxs-lookup"><span data-stu-id="0679b-111">\\\\.\\mailslot\\taxes\\petes\_comments</span></span>  
<span data-ttu-id="0679b-112">\\\\.\\ \\comentarios de \\ usa de impuestos de buzón de correo \_</span><span class="sxs-lookup"><span data-stu-id="0679b-112">\\\\.\\mailslot\\taxes\\sues\_comments</span></span>  
</dl>

<span data-ttu-id="0679b-113">Para colocar un mensaje en un buzón de correo, un proceso abre un buzón de correo por nombre.</span><span class="sxs-lookup"><span data-stu-id="0679b-113">To put a message into a mailslot, a process opens a mailslot by name.</span></span> <span data-ttu-id="0679b-114">Para escribir en un buzón de correo en el equipo local, un proceso puede usar un nombre de buzón de correo que tenga el mismo formato que se usa para crear un buzón de correo.</span><span class="sxs-lookup"><span data-stu-id="0679b-114">To write to a mailslot on the local computer, a process can use a mailslot name that has the same form used for creating a mailslot.</span></span> <span data-ttu-id="0679b-115">Sin embargo, esta situación es relativamente poco frecuente.</span><span class="sxs-lookup"><span data-stu-id="0679b-115">This situation, however, is relatively uncommon.</span></span> <span data-ttu-id="0679b-116">Con más frecuencia, usaría el siguiente formato para escribir en un buzón de correo en un equipo remoto específico:</span><span class="sxs-lookup"><span data-stu-id="0679b-116">More frequently, you would use the following form to write to a mailslot on a specific remote computer:</span></span>

<span data-ttu-id="0679b-117">\\\\*Nombre del equipo* \\ nombre de \\ \[ *ruta de acceso* \\ \]  de buzón</span><span class="sxs-lookup"><span data-stu-id="0679b-117">\\\\*ComputerName*\\mailslot\\\[*path*\\\]*name*</span></span>

<span data-ttu-id="0679b-118">Para colocar un mensaje en cada buzón de correo del dominio especificado con un nombre determinado, use el formato siguiente:</span><span class="sxs-lookup"><span data-stu-id="0679b-118">To put a message into every mailslot in the specified domain with a given name, use the following form:</span></span>

<span data-ttu-id="0679b-119">\\\\*Dominio* \\ de nombre de \\ \[ *ruta de acceso* \\ \]  de buzón</span><span class="sxs-lookup"><span data-stu-id="0679b-119">\\\\*DomainName*\\mailslot\\\[*path*\\\]*name*</span></span>

<span data-ttu-id="0679b-120">Para colocar un mensaje en cada buzón de correo con un nombre determinado en el dominio principal del sistema, utilice el formato siguiente:</span><span class="sxs-lookup"><span data-stu-id="0679b-120">To put a message into every mailslot with a given name in the system's primary domain, use the following form:</span></span>

<span data-ttu-id="0679b-121">\\\\\*\\nombre de \\ \[ *ruta de acceso* \\ \]  de buzón</span><span class="sxs-lookup"><span data-stu-id="0679b-121">\\\\\*\\mailslot\\\[*path*\\\]*name*</span></span>

 

 



