---
description: Hay situaciones en las que las claves se deben exportar desde el entorno seguro del proveedor de servicios criptográficos (CSP) al espacio de datos de una aplicación. Las claves que se han exportado se almacenan en estructuras BLOB de clave cifrada.
ms.assetid: 859b1bfe-6182-4728-a721-1f34cc98f66f
title: Almacenamiento de claves criptográficas y Exchange
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: be7e789a736f0fcd5208bc16d73b43c6a9232e33
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105666417"
---
# <a name="cryptographic-key-storage-and-exchange"></a><span data-ttu-id="b83db-104">Almacenamiento de claves criptográficas y Exchange</span><span class="sxs-lookup"><span data-stu-id="b83db-104">Cryptographic Key Storage and Exchange</span></span>

<span data-ttu-id="b83db-105">Hay situaciones en las que las claves se deben exportar desde el entorno seguro del [*proveedor de servicios criptográficos*](../secgloss/c-gly.md) (CSP) al espacio de datos de una aplicación.</span><span class="sxs-lookup"><span data-stu-id="b83db-105">There are situations where keys must be exported from the secure environment of the [*cryptographic service provider*](../secgloss/c-gly.md) (CSP) into an application's data space.</span></span> <span data-ttu-id="b83db-106">Las claves que se han exportado se almacenan en estructuras [*BLOB de clave*](../secgloss/k-gly.md) cifrada.</span><span class="sxs-lookup"><span data-stu-id="b83db-106">Keys that have been exported are stored in encrypted [*key BLOB*](../secgloss/k-gly.md) structures.</span></span>

<span data-ttu-id="b83db-107">Hay dos situaciones específicas en las que es necesario exportar claves:</span><span class="sxs-lookup"><span data-stu-id="b83db-107">There are two specific situations where it is necessary to export keys:</span></span>

-   <span data-ttu-id="b83db-108">Para guardar una [*clave de sesión*](../secgloss/s-gly.md) para su uso posterior por parte de una aplicación, si, por ejemplo, una aplicación acaba de cifrar un archivo de base de datos para descifrarlo más adelante.</span><span class="sxs-lookup"><span data-stu-id="b83db-108">To save a [*session key*](../secgloss/s-gly.md) for later use by an application, if, for example, an application has just encrypted a database file to be decrypted at a later time.</span></span> <span data-ttu-id="b83db-109">La aplicación es responsable de almacenar la clave de cifrado.</span><span class="sxs-lookup"><span data-stu-id="b83db-109">The application is responsible for storing the encryption key.</span></span> <span data-ttu-id="b83db-110">Esto es necesario porque los CSP no conservan [*las claves simétricas*](../secgloss/s-gly.md) de la sesión en la sesión.</span><span class="sxs-lookup"><span data-stu-id="b83db-110">This is necessary because CSPs do not preserve [*symmetric keys*](../secgloss/s-gly.md) from session to session.</span></span>
-   <span data-ttu-id="b83db-111">Para enviar una clave a otra persona.</span><span class="sxs-lookup"><span data-stu-id="b83db-111">To send a key to someone else.</span></span> <span data-ttu-id="b83db-112">Esto sería más fácil si los CSP correspondientes pudieran comunicarse directamente, pero no.</span><span class="sxs-lookup"><span data-stu-id="b83db-112">This would be easier if the respective CSPs could communicate directly, but they cannot.</span></span> <span data-ttu-id="b83db-113">Dado que los CSP no se pueden comunicar, la clave debe exportarse de un CSP, transmitirse a la aplicación de destino y, a continuación, importarse en el CSP de destino.</span><span class="sxs-lookup"><span data-stu-id="b83db-113">Because CSPs cannot communicate, the key has to be exported from one CSP, transmitted to the destination application, and then imported into the destination CSP.</span></span> <span data-ttu-id="b83db-114">Este proceso puede ser más complicado si la ruta de comunicación no es de confianza.</span><span class="sxs-lookup"><span data-stu-id="b83db-114">This process can become more complicated if the communication path is not trusted.</span></span>

<span data-ttu-id="b83db-115">En cualquier caso, una aplicación debe almacenar una clave de sesión fuera del CSP durante un período de tiempo.</span><span class="sxs-lookup"><span data-stu-id="b83db-115">In either case, an application must store a session key outside the CSP for a period of time.</span></span> <span data-ttu-id="b83db-116">Para obtener más información, consulte [procedimiento para almacenar una clave de sesión](procedure-for-storing-a-session-key.md).</span><span class="sxs-lookup"><span data-stu-id="b83db-116">For more information, see [Procedure for Storing a Session Key](procedure-for-storing-a-session-key.md).</span></span>

 

 
