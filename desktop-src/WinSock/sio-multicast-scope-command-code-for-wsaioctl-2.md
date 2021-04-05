---
description: Cuando se emplea la multidifusión, normalmente es necesario especificar el ámbito en el que se debe producir la multidifusión.
ms.assetid: 744b43a8-dd89-4e63-ae3c-5bee72864df7
title: Código de comando de SIO_MULTICAST_SCOPE para WSAIoctl
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 209a43e461907dcded8e59c6ffee9b1376989d6e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104082399"
---
# <a name="sio_multicast_scope-command-code-for-wsaioctl"></a><span data-ttu-id="a5623-103">\_ \_ Código de comando de ámbito de multidifusión de SiO para WSAIoctl</span><span class="sxs-lookup"><span data-stu-id="a5623-103">SIO\_MULTICAST\_SCOPE Command Code for WSAIoctl</span></span>

<span data-ttu-id="a5623-104">Cuando se emplea la multidifusión, normalmente es necesario especificar el *ámbito* en el que se debe producir la multidifusión.</span><span class="sxs-lookup"><span data-stu-id="a5623-104">When multicasting is employed, it is usually necessary to specify the *scope* over which the multicast should occur.</span></span> <span data-ttu-id="a5623-105">El ámbito se define como el número de segmentos de red enrutados que se van a cubrir.</span><span class="sxs-lookup"><span data-stu-id="a5623-105">Scope is defined as the number of routed network segments to be covered.</span></span> <span data-ttu-id="a5623-106">Un ámbito de cero indicaría que la transmisión por multidifusión no se colocaría en la conexión, pero podría diseminarse a través de sockets dentro del host local.</span><span class="sxs-lookup"><span data-stu-id="a5623-106">A scope of zero would indicate that the multicast transmission would not be placed on the wire but could be disseminated across sockets within the local host.</span></span> <span data-ttu-id="a5623-107">Un valor de ámbito de 1 (valor predeterminado) indica que la transmisión se colocará en la conexión, pero no cruzará ningún enrutador.</span><span class="sxs-lookup"><span data-stu-id="a5623-107">A scope value of 1 (the default) indicates that the transmission will be placed on the wire, but will not cross any routers.</span></span> <span data-ttu-id="a5623-108">Los valores de ámbito más altos determinan el número de enrutadores que se pueden cruzar.</span><span class="sxs-lookup"><span data-stu-id="a5623-108">Higher scope values determine the number of routers that may be crossed.</span></span> <span data-ttu-id="a5623-109">Tenga en cuenta que esto corresponde al parámetro Time-to-Live (TTL) de la multidifusión IP.</span><span class="sxs-lookup"><span data-stu-id="a5623-109">Note that this corresponds to the time-to-live (TTL) parameter in IP multicasting.</span></span>

<span data-ttu-id="a5623-110">La función [**WSAJoinLeaf**](/windows/desktop/api/Winsock2/nf-winsock2-wsajoinleaf) se usa para unir un nodo hoja a la sesión multipoint.</span><span class="sxs-lookup"><span data-stu-id="a5623-110">The function [**WSAJoinLeaf**](/windows/desktop/api/Winsock2/nf-winsock2-wsajoinleaf) is used to join a leaf node into the multipoint session.</span></span> <span data-ttu-id="a5623-111">Vea lo siguiente para obtener una explicación sobre cómo se emplea esta función.</span><span class="sxs-lookup"><span data-stu-id="a5623-111">See the following for a discussion on how this function is utilized.</span></span>

 

 



