---
title: Coherencia de la transferencia de archivos
description: BITS garantiza que la versión del archivo que transfiere es coherente según el tamaño del archivo y la marca de tiempo, no el contenido (BITS no protege contra ataques de tipo "Man in the Middle").
ms.assetid: ba82f172-a3ac-49d6-bccd-7d0b68ba66de
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 533bc0c0db9708528d4ae919572d6e4c1d251ac8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103903140"
---
# <a name="file-transfer-consistency"></a><span data-ttu-id="2ff36-103">Coherencia de la transferencia de archivos</span><span class="sxs-lookup"><span data-stu-id="2ff36-103">File Transfer Consistency</span></span>

<span data-ttu-id="2ff36-104">BITS garantiza que la versión del archivo que transfiere es coherente según el tamaño del archivo y la marca de tiempo, no el contenido (BITS no protege contra ataques de tipo "Man in the Middle").</span><span class="sxs-lookup"><span data-stu-id="2ff36-104">BITS guarantees that the version of the file it transfers is consistent based on the file size and time stamp, not content (BITS does not protect against man-in-the-middle attacks).</span></span> <span data-ttu-id="2ff36-105">Para comprobar el contenido usted mismo, puede usar el método [**IBackgroundCopyFile3:: GetTemporaryName**](/windows/desktop/api/Bits3_0/nf-bits3_0-ibackgroundcopyfile3-gettemporaryname) para obtener el nombre del archivo que contiene el contenido descargado, comprobar el contenido mediante su propio mecanismo y, a continuación, llamar al método [**IBackgroundCopyFile3:: SetValidationState**](/windows/desktop/api/Bits3_0/nf-bits3_0-ibackgroundcopyfile3-setvalidationstate) para indicar a bits si el contenido del archivo es válido.</span><span class="sxs-lookup"><span data-stu-id="2ff36-105">To verify the contents yourself, you can use the [**IBackgroundCopyFile3::GetTemporaryName**](/windows/desktop/api/Bits3_0/nf-bits3_0-ibackgroundcopyfile3-gettemporaryname) method to get the name of the file that contains the downloaded content, verify the contents using your own mechanism, and then call the [**IBackgroundCopyFile3::SetValidationState**](/windows/desktop/api/Bits3_0/nf-bits3_0-ibackgroundcopyfile3-setvalidationstate) method to indicate to BITS if the contents of the file is valid.</span></span> <span data-ttu-id="2ff36-106">Si establece el estado de validación en **false** y el contenido procede del servidor de origen, el trabajo entra en el estado de error.</span><span class="sxs-lookup"><span data-stu-id="2ff36-106">If you set the validation state to **FALSE** and the content is from the origin server, the job goes into the error state.</span></span> <span data-ttu-id="2ff36-107">Si el contenido procede de un elemento del mismo nivel, BITS descargará el archivo desde el servidor de origen.</span><span class="sxs-lookup"><span data-stu-id="2ff36-107">If the content is from a peer, BITS downloads the file from the origin server.</span></span>

<span data-ttu-id="2ff36-108">En el caso de las descargas, si el tamaño de archivo o la marca de tiempo cambian mientras BITS está transfiriendo el archivo, BITS reinicia la transferencia de ese archivo únicamente.</span><span class="sxs-lookup"><span data-stu-id="2ff36-108">For downloads, if the file size or time stamp changes while BITS is transferring the file, BITS restarts the transfer of that file only.</span></span> <span data-ttu-id="2ff36-109">Por ejemplo, si el trabajo de descarga contiene dos archivos y los archivos se actualizan en el servidor mientras BITS está transfiriendo el segundo archivo, BITS reinicia la transferencia del segundo archivo únicamente.</span><span class="sxs-lookup"><span data-stu-id="2ff36-109">For example, if the download job contains two files and the files are updated on the server while BITS is transferring the second file, BITS restarts the transfer of the second file only.</span></span> <span data-ttu-id="2ff36-110">El primer archivo, que ya se transfirió correctamente, no se actualiza para reflejar los nuevos cambios.</span><span class="sxs-lookup"><span data-stu-id="2ff36-110">The first file, which already transferred successfully, is not updated to reflect the new changes.</span></span>

<span data-ttu-id="2ff36-111">Tenga en cuenta que si es el propietario del archivo que se está descargando del servidor, debe crear una nueva dirección URL para cada nueva versión del archivo.</span><span class="sxs-lookup"><span data-stu-id="2ff36-111">Note that if you own the file being downloaded from the server, you should create a new URL for each new version of the file.</span></span> <span data-ttu-id="2ff36-112">Si usa la misma dirección URL para las nuevas versiones del archivo, algunos servidores proxy pueden servir datos obsoletos de la memoria caché porque no se comprueban con el servidor original si el archivo está obsoleto.</span><span class="sxs-lookup"><span data-stu-id="2ff36-112">If you use the same URL for new versions of the file, some proxy servers may serve stale data from their cache because they do not verify with the original server if the file is stale.</span></span>

<span data-ttu-id="2ff36-113">En el caso de las cargas, si el tamaño de archivo o la marca de tiempo cambian durante la transferencia de archivos, BITS genera un error y el trabajo se coloca en el estado de error de estado de trabajo de BG \_ \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="2ff36-113">For uploads, if the file size or time stamp changes during the file transfer, BITS generates an error and the job is placed in the BG\_JOB\_STATE\_ERROR state.</span></span>

<span data-ttu-id="2ff36-114">BITS no sincroniza las solicitudes de transferencia cuando uno o varios usuarios solicitan que el mismo archivo se transfiera a la misma ubicación.</span><span class="sxs-lookup"><span data-stu-id="2ff36-114">BITS does not synchronize transfer requests when one or more users request that the same file be transferred to the same location.</span></span> <span data-ttu-id="2ff36-115">BITS transfiere el archivo para cada solicitud por separado.</span><span class="sxs-lookup"><span data-stu-id="2ff36-115">BITS transfers the file for each request separately.</span></span>

 

 




