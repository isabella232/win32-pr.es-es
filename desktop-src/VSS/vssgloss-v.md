---
description: A B C D E F G H I J K L M N O P Q R S T U V W X Y Z
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: cbaa7eff-a88b-4b0e-b7b5-5c0d99397942
title: V (Servicio de instantáneas de volumen)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6da999c820e7a18ce27fc6fac144f88d1d1dafee
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104541718"
---
# <a name="v-volume-shadow-copy-service"></a><span data-ttu-id="2056c-103">V (Servicio de instantáneas de volumen)</span><span class="sxs-lookup"><span data-stu-id="2056c-103">V (Volume Shadow Copy Service)</span></span>

<span data-ttu-id="2056c-104">[A](vssgloss-a.md) [B](vssgloss-b.md) [C](vssgloss-c.md) [D](vssgloss-d.md) [E](vssgloss-e.md) [F](vssgloss-f.md) [G](vssgloss-g.md) [H](vssgloss-h.md) [I](vssgloss-i.md) J K [L](vssgloss-l.md) M [N](vssgloss-n.md) [o](vssgloss-o.md) [p](vssgloss-p.md) Q [R](vssgloss-r.md) [s](vssgloss-s.md) [T](vssgloss-t.md) U V [W](vssgloss-w.md) X Y Z</span><span class="sxs-lookup"><span data-stu-id="2056c-104">[A](vssgloss-a.md) [B](vssgloss-b.md) [C](vssgloss-c.md) [D](vssgloss-d.md) [E](vssgloss-e.md) [F](vssgloss-f.md) [G](vssgloss-g.md) [H](vssgloss-h.md) [I](vssgloss-i.md) J K [L](vssgloss-l.md) M [N](vssgloss-n.md) [O](vssgloss-o.md) [P](vssgloss-p.md) Q [R](vssgloss-r.md) [S](vssgloss-s.md) [T](vssgloss-t.md) U V [W](vssgloss-w.md) X Y Z</span></span>

<dl> <dt>

<span data-ttu-id="2056c-105"><span id="base.vssgloss_volume"></span><span id="BASE.VSSGLOSS_VOLUME"></span>**cantidad**</span><span class="sxs-lookup"><span data-stu-id="2056c-105"><span id="base.vssgloss_volume"></span><span id="BASE.VSSGLOSS_VOLUME"></span>**volume**</span></span>
</dt> <dd>

<span data-ttu-id="2056c-106">Una unidad de almacenamiento lógico.</span><span class="sxs-lookup"><span data-stu-id="2056c-106">A logical storage unit.</span></span> <span data-ttu-id="2056c-107">Un volumen es el destino de las operaciones de creación de instantáneas.</span><span class="sxs-lookup"><span data-stu-id="2056c-107">A volume is the target of shadow copy creation operations.</span></span>

</dd> <dt>

<span data-ttu-id="2056c-108"><span id="base.vssgloss_volume_name"></span><span id="BASE.VSSGLOSS_VOLUME_NAME"></span>**nombre del GUID de volumen**</span><span class="sxs-lookup"><span data-stu-id="2056c-108"><span id="base.vssgloss_volume_name"></span><span id="BASE.VSSGLOSS_VOLUME_NAME"></span>**volume GUID name**</span></span>
</dt> <dd>

<span data-ttu-id="2056c-109">Un nombre único para un volumen.</span><span class="sxs-lookup"><span data-stu-id="2056c-109">A unique name for a volume.</span></span> <span data-ttu-id="2056c-110">Un nombre de GUID de volumen es una cadena con el formato siguiente:</span><span class="sxs-lookup"><span data-stu-id="2056c-110">A volume GUID name is a string of the following form:</span></span>

<span data-ttu-id="2056c-111">\\\\?\\ Volumen {GUID}</span><span class="sxs-lookup"><span data-stu-id="2056c-111">\\\\?\\Volume{GUID}</span></span>\\

<span data-ttu-id="2056c-112">(observe el carácter " \\ "), donde GUID es un identificador único global para el volumen.</span><span class="sxs-lookup"><span data-stu-id="2056c-112">(note the trailing "\\") where GUID is a globally unique identifier for the volume.</span></span> <span data-ttu-id="2056c-113">El sistema operativo asigna un nombre de volumen cuando encuentra por primera vez un volumen, por ejemplo, durante el formato o la instalación.</span><span class="sxs-lookup"><span data-stu-id="2056c-113">The operating system assigns a volume name when it first encounters a volume, for example, during formatting or installation.</span></span>

<span data-ttu-id="2056c-114">Tenga en cuenta que un volumen puede tener más de un nombre de GUID de volumen.</span><span class="sxs-lookup"><span data-stu-id="2056c-114">Note that a volume can have more than one volume GUID name.</span></span>

</dd> </dl>

 

 



