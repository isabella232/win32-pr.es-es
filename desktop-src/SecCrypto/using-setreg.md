---
description: La herramienta SetReg establece el valor de las claves del registro que controlan el comportamiento del proceso de comprobación de certificados Authenticode.
ms.assetid: c34c00fe-da99-4c2e-9e9a-0ef6406ae5ae
title: Usar SetReg
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 706463f86d38a03bc3416713be7427df55424d09
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104155084"
---
# <a name="using-setreg"></a><span data-ttu-id="1b969-103">Usar SetReg</span><span class="sxs-lookup"><span data-stu-id="1b969-103">Using SetReg</span></span>

<span data-ttu-id="1b969-104">La herramienta SetReg establece el valor de las claves del registro que controlan el comportamiento del proceso de comprobación de certificados Authenticode.</span><span class="sxs-lookup"><span data-stu-id="1b969-104">The SetReg tool sets the value of the registry keys controlling the behavior of the Authenticode certificate verification process.</span></span> <span data-ttu-id="1b969-105">Estas claves, denominadas claves de estado de publicación de software, controlan si se confía en una raíz de prueba, permiten la aprobación sin conexión de certificados, las fechas de expiración de certificado de prueba y realizan comprobaciones de revocación.</span><span class="sxs-lookup"><span data-stu-id="1b969-105">These keys, called the Software Publishing State Keys, control whether to trust a test root, allow offline approval of certificates, test certificate expiration dates, and perform revocation checks.</span></span>

<span data-ttu-id="1b969-106">El siguiente comando muestra la sintaxis y las opciones para usar SetReg.</span><span class="sxs-lookup"><span data-stu-id="1b969-106">The following command lists the syntax and options for using SetReg.</span></span>

<span data-ttu-id="1b969-107">**setreg-?**</span><span class="sxs-lookup"><span data-stu-id="1b969-107">**setreg -?**</span></span>

<span data-ttu-id="1b969-108">El comando siguiente hace que se confíe en una raíz de prueba.</span><span class="sxs-lookup"><span data-stu-id="1b969-108">The following command makes a test root trusted.</span></span> <span data-ttu-id="1b969-109">De forma predeterminada, una raíz de prueba no es de confianza.</span><span class="sxs-lookup"><span data-stu-id="1b969-109">By default, a test root is not trusted.</span></span> <span data-ttu-id="1b969-110">Una vez realizados los cambios en los valores de clave, se muestra una lista del valor actual de todos los valores de clave.</span><span class="sxs-lookup"><span data-stu-id="1b969-110">After any changes in the key values are made, a list of the current value of all of the key values is displayed.</span></span> <span data-ttu-id="1b969-111">Si se usa la opción **-q** , no se muestran los valores de clave.</span><span class="sxs-lookup"><span data-stu-id="1b969-111">If the **-q** option is used, the key values are not displayed.</span></span>

<span data-ttu-id="1b969-112">**setreg 1 TRUE**</span><span class="sxs-lookup"><span data-stu-id="1b969-112">**setreg 1 TRUE**</span></span>

<span data-ttu-id="1b969-113">El comando siguiente hace que una raíz de prueba no sea de confianza y hace que toda la comprobación Compruebe la revocación.</span><span class="sxs-lookup"><span data-stu-id="1b969-113">The following command makes a test root untrusted and causes all verification to check for revocation.</span></span> <span data-ttu-id="1b969-114">Se usa la opción **-q** para que no se muestre la lista de valores de clave.</span><span class="sxs-lookup"><span data-stu-id="1b969-114">The **-q** option is used so that the list of key values is not displayed</span></span>

<span data-ttu-id="1b969-115">**setreg-q 1 falso 3 TRUE**</span><span class="sxs-lookup"><span data-stu-id="1b969-115">**setreg -q 1 FALSE 3 TRUE**</span></span>

> [!Note]  
> <span data-ttu-id="1b969-116">Los comandos, las opciones y los argumentos no distinguen mayúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="1b969-116">Commands, options, and arguments are not case sensitive.</span></span>

 

 

 



