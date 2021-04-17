---
description: Además de tener acceso a través de la interfaz IVssBackupComponents mediante el objeto de dispositivo de la copia, un solicitante puede hacer que una instantánea esté disponible para otros procesos como un dispositivo montado de solo lectura.
ms.assetid: 0898c2dc-992a-411b-81df-4f5e129f6a80
title: Exposición y exposición de volúmenes de copia sombra
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d684aa9b696facaf1caa3aa3102c6b1d7fc37409
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105697740"
---
# <a name="exposing-and-surfacing-shadow-copied-volumes"></a><span data-ttu-id="5bd8d-103">Exposición y exposición de volúmenes de copia sombra</span><span class="sxs-lookup"><span data-stu-id="5bd8d-103">Exposing and Surfacing Shadow Copied Volumes</span></span>

<span data-ttu-id="5bd8d-104">Además de tener acceso a través de la interfaz [**IVssBackupComponents**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssbackupcomponents) mediante el [*objeto de dispositivo*](vssgloss-d.md)de la copia, un solicitante puede hacer que una instantánea esté disponible para otros procesos como un dispositivo montado de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="5bd8d-104">In addition to being accessed through the [**IVssBackupComponents**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssbackupcomponents) interface by means of its copy's [*device object*](vssgloss-d.md), a requester can make a shadow copy available to other processes as a mounted read-only device.</span></span>

<span data-ttu-id="5bd8d-105">Este proceso se conoce como [*exponer una instantánea*](vssgloss-e.md)y se realiza mediante el método [**IVssBackupComponents:: ExposeSnapshot**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-exposesnapshot) .</span><span class="sxs-lookup"><span data-stu-id="5bd8d-105">This process is known as [*exposing a shadow copy*](vssgloss-e.md), and is performed using the [**IVssBackupComponents::ExposeSnapshot**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-exposesnapshot) method.</span></span>

<span data-ttu-id="5bd8d-106">Una instantánea se puede exponer como un volumen local (se le asigna una letra de unidad o se asocia a una carpeta montada) o como un recurso compartido de archivos.</span><span class="sxs-lookup"><span data-stu-id="5bd8d-106">A shadow copy can be exposed as a local volume—assigned a drive letter or associated with a mounted folder—or as a file share.</span></span>

<span data-ttu-id="5bd8d-107">Para ilustrar, considere la posibilidad de usar una instantánea de un volumen en el sistema exposedSys montado en F: \\ en cuya raíz sean los directorios dirOne y dirTwo, y el archivo FileOne.</span><span class="sxs-lookup"><span data-stu-id="5bd8d-107">To illustrate, consider a shadow copy made of a volume on the system exposedSys mounted at F:\\ on whose root are the directories dirOne and dirTwo, and the file FileOne.</span></span>

## <a name="exposing-a-shadow-copy-locally"></a><span data-ttu-id="5bd8d-108">Exponer una instantánea localmente</span><span class="sxs-lookup"><span data-stu-id="5bd8d-108">Exposing a Shadow Copy Locally</span></span>

<span data-ttu-id="5bd8d-109">Cuando se monta como un volumen local, la raíz de la instantánea siempre es visible en el punto de montaje (letra de unidad o carpeta montada) y todos los archivos de copia sombra están visibles.</span><span class="sxs-lookup"><span data-stu-id="5bd8d-109">When mounted as a local volume, the shadow copy's root is always visible at the mount point (drive letter or mounted folder) and all the shadow-copied files are visible.</span></span>

<span data-ttu-id="5bd8d-110">Si la instantánea se expuso localmente a través de la carpeta montada C: \\ ShadowOfF, encontraría todos los archivos presentes en el disco montados en F: \\ en el momento de la instantánea disponible en C: \\ ShadowOfF.</span><span class="sxs-lookup"><span data-stu-id="5bd8d-110">If the shadow copy was locally exposed through the mounted folder C:\\ShadowOfF, you would find all files present on disk mounted at F:\\ at the time of the shadow copy available under C:\\ShadowOfF.</span></span> <span data-ttu-id="5bd8d-111">El examen de C: \\ ShadowOfF revelaría dos directorios, dirOne y dirTwo, y un archivo, fileOne, en C: \\ ShadowOfF.</span><span class="sxs-lookup"><span data-stu-id="5bd8d-111">Examining C:\\ShadowOfF would reveal two directories, dirOne and dirTwo, and one file, fileOne, under C:\\ShadowOfF.</span></span>

<span data-ttu-id="5bd8d-112">Una llamada a exponer localmente la instantánea podría ser:</span><span class="sxs-lookup"><span data-stu-id="5bd8d-112">A call to locally expose the shadow copy might be:</span></span>

``` syntax
  IVssBackupComponents *pReq;
  VSS_ID snapID;
  PWSTR wszExposed;
  //    .
  //    .
  hr = pReg->ExposeSnapshot(
         snapID,                           // VSS_ID SnapshotId,
         NULL,                             // VSS_PWSZ wszPathFromRoot
         VSS_VOLSNAP_ATTR_EXPOSED_LOCALLY, // LONG lAttributes
         L"C:\ShadowOfF",                  // VSS_PWSZ wszExpose
         LPWSTR &wszExposed,               // VSS_PWSZ* pwszExposed
       );
```

<span data-ttu-id="5bd8d-113">Si la instantánea se ha expuesto correctamente localmente, *wszExposed* debe contener la cadena de caracteres anchos "C: \\ ShadowOfF".</span><span class="sxs-lookup"><span data-stu-id="5bd8d-113">If the shadow copy was successfully exposed locally, *wszExposed* should contain the wide character string "C:\\ShadowOfF."</span></span>

<span data-ttu-id="5bd8d-114">La instantánea se puede no exponer más adelante llamando a [**IVssBackupComponentsEx2:: UnexposeSnapshot**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponentsex2-unexposesnapshot).</span><span class="sxs-lookup"><span data-stu-id="5bd8d-114">The shadow copy can later be unexposed by calling [**IVssBackupComponentsEx2::UnexposeSnapshot**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponentsex2-unexposesnapshot).</span></span>

<span data-ttu-id="5bd8d-115">Solo las instantáneas persistentes, es decir, las instantáneas creadas con la \_ reversión de NAS de VSS CTX \_ o la reversión de la \_ aplicación de VSS \_ CTX \_ \_ , se pueden exponer localmente.</span><span class="sxs-lookup"><span data-stu-id="5bd8d-115">Only persistent shadow copies—that is, shadow copies created with either VSS\_CTX\_NAS\_ROLLBACK or VSS\_CTX\_APP\_ROLLBACK—can be exposed locally.</span></span>

## <a name="exposing-a-shadow-copy-as-a-remote-share"></a><span data-ttu-id="5bd8d-116">Exponer una instantánea como un recurso compartido remoto</span><span class="sxs-lookup"><span data-stu-id="5bd8d-116">Exposing a Shadow Copy as a Remote Share</span></span>

<span data-ttu-id="5bd8d-117">Como alternativa, puede elegir hacer que la instantánea del disco esté montada en F: \\ disponible como un recurso compartido de archivos remoto y exponer solo los datos en dirTwo como el recurso compartido de archivos dirTwoOfF.</span><span class="sxs-lookup"><span data-stu-id="5bd8d-117">Alternatively, you could choose to make the shadow copy of the disk mounted at F:\\ available as a remote file share, and expose only data under dirTwo as the file share dirTwoOfF.</span></span>

<span data-ttu-id="5bd8d-118">En este caso, los sistemas pueden obtener acceso a la instantánea de archivos en F: dirTwo asignando \\ \\ \\ exposedSys \\ dirTwoOfF como unidad de red.</span><span class="sxs-lookup"><span data-stu-id="5bd8d-118">In this case, systems could access the shadow copy of files under F:\\dirTwo by mapping \\\\exposedSys\\dirTwoOfF as a network drive.</span></span>

<span data-ttu-id="5bd8d-119">Una llamada para implementar la exposición remota de la instantánea como un recurso compartido podría ser la siguiente:</span><span class="sxs-lookup"><span data-stu-id="5bd8d-119">A call to implement remote exposing the shadow copy as a share might be the following:</span></span>

``` syntax
  IVssBackupComponents *pReq;
  VSS_ID snapID;
  LPWSTR wszExposed;
  //    .
  //    .
  hr = pReg->ExposeSnapshot(
               snapID,                            // VSS_ID SnapshotId,
               L"\dirTwo",                        // VSS_PWSZ wszPathFromRoot
               VSS_VOLSNAP_ATTR_EXPOSED_REMOTELY, // LONG lAttributes
               L"dirTwoOfF",                      // VSS_PWSZ wszExpose
               LPWSTR &wszExposed,                // VSS_PWSZ* pwszExposed
       );
```

<span data-ttu-id="5bd8d-120">Si la instantánea se expone correctamente de forma remota, *wszExposed* debe contener la cadena de caracteres anchos "dirTwoOfF".</span><span class="sxs-lookup"><span data-stu-id="5bd8d-120">If the shadow copy was successfully exposed remotely, *wszExposed* should contain the wide character string "dirTwoOfF."</span></span>

<span data-ttu-id="5bd8d-121">Cualquier sistema que asigne actualmente el recurso compartido de red de dirTwoOfF podría desconectarse de ella, de la misma forma que podría desconectarse de cualquier recurso compartido normal.</span><span class="sxs-lookup"><span data-stu-id="5bd8d-121">Any system currently mapping the network share of dirTwoOfF could disconnect from it, just as it might disconnect from any ordinary share.</span></span>

## <a name="surfacing-a-shadow-copy"></a><span data-ttu-id="5bd8d-122">Exponer una instantánea</span><span class="sxs-lookup"><span data-stu-id="5bd8d-122">Surfacing a Shadow Copy</span></span>

<span data-ttu-id="5bd8d-123">Una instantánea [*superficial*](vssgloss-s.md) es aquella en la que el espacio de nombres del administrador de montaje de un sistema conoce la instantánea.</span><span class="sxs-lookup"><span data-stu-id="5bd8d-123">A [*surfaced shadow copy*](vssgloss-s.md) is one in which the shadow copy is known to a system's Mount Manager namespace.</span></span>

<span data-ttu-id="5bd8d-124">Esto significa que puede buscar dichas instantáneas tal y como ubicaría cualquier otro volumen disponible pero que no esté montado, mediante **FindFirstVolume** y **FindNextVolume**, por ejemplo.</span><span class="sxs-lookup"><span data-stu-id="5bd8d-124">This means that you can locate such shadow copies just as you would locate any other available but not-yet-mounted volume—by using **FindFirstVolume** and **FindNextVolume**, for example.</span></span>

<span data-ttu-id="5bd8d-125">Claramente, las instantáneas expuestas también son instantáneas superficiales.</span><span class="sxs-lookup"><span data-stu-id="5bd8d-125">Clearly, then, exposed shadow copies are also surfaced shadow copies.</span></span> <span data-ttu-id="5bd8d-126">Sin embargo, la inversa no es necesariamente verdadera.</span><span class="sxs-lookup"><span data-stu-id="5bd8d-126">However, the reverse is not necessarily true.</span></span>

<span data-ttu-id="5bd8d-127">Si se desmontó una instantánea expuesta localmente, o un sistema decidió desconectar una instantánea expuesta de forma remota, esa instantánea ya no se expondría.</span><span class="sxs-lookup"><span data-stu-id="5bd8d-127">If a locally exposed shadow copy was dismounted, or a system chose to disconnect a remotely exposed shadow copy, that shadow copy would no longer be exposed.</span></span> <span data-ttu-id="5bd8d-128">Sin embargo, siempre y cuando la instantánea persista, los volúmenes se verán en la superficie.</span><span class="sxs-lookup"><span data-stu-id="5bd8d-128">However, as long as the shadow copy persisted, the volumes would be surfaced.</span></span> <span data-ttu-id="5bd8d-129">Esto significa que podrían montarse como cualquier otro volumen de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="5bd8d-129">This means they could be mounted like any other read-only volume.</span></span>

 

 



