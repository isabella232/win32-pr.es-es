---
title: Comunicación de componentes del lado servidor y del cliente NAP
description: Comunicación de componentes del lado servidor y del cliente NAP
ms.assetid: 7658cf0c-607b-44ba-b579-72082d0d1f51
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 07597ac80a1e02c4f8528b3c99050aefb5963988
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104419050"
---
# <a name="nap-client-and-server-side-component-communication"></a><span data-ttu-id="091c5-103">Comunicación de componentes del lado servidor y del cliente NAP</span><span class="sxs-lookup"><span data-stu-id="091c5-103">NAP Client and Server-side Component Communication</span></span>

> [!Note]  
> <span data-ttu-id="091c5-104">La plataforma de protección de acceso a redes no está disponible a partir de Windows 10</span><span class="sxs-lookup"><span data-stu-id="091c5-104">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="091c5-105">El componente agente NAP puede comunicarse con el componente de servidor de administración de NAP a través del proceso siguiente:</span><span class="sxs-lookup"><span data-stu-id="091c5-105">The NAP Agent component can communicate with the NAP Administration Server component through the following process:</span></span>

1.  <span data-ttu-id="091c5-106">El agente NAP pasa el SSoH a NAP EC.</span><span class="sxs-lookup"><span data-stu-id="091c5-106">The NAP Agent passes the SSoH to the NAP EC.</span></span>
2.  <span data-ttu-id="091c5-107">El NAP EC pasa el SSoH a NAP.</span><span class="sxs-lookup"><span data-stu-id="091c5-107">The NAP EC passes the SSoH to the NAP ES.</span></span>
3.  <span data-ttu-id="091c5-108">NAP ES pasa el SSoH al servicio del servidor de directivas de redes (NPS).</span><span class="sxs-lookup"><span data-stu-id="091c5-108">The NAP ES passes the SSoH to the Network Policy Server (NPS) service.</span></span>
4.  <span data-ttu-id="091c5-109">El servicio NPS pasa el SSoH al servidor de administración de NAP.</span><span class="sxs-lookup"><span data-stu-id="091c5-109">The NPS service passes the SSoH to the NAP Administration Server.</span></span>

<span data-ttu-id="091c5-110">Un SHA puede comunicarse con su SHV correspondiente a través del proceso siguiente:</span><span class="sxs-lookup"><span data-stu-id="091c5-110">An SHA can communicate with its corresponding SHV through the following process:</span></span>

1.  <span data-ttu-id="091c5-111">SHA pasa su SoH al agente NAP.</span><span class="sxs-lookup"><span data-stu-id="091c5-111">The SHA passes its SoH to the NAP Agent.</span></span>
2.  <span data-ttu-id="091c5-112">El agente NAP pasa el SoH, contenido dentro de SSoH, al NAP EC.</span><span class="sxs-lookup"><span data-stu-id="091c5-112">The NAP Agent passes the SoH, contained within the SSoH, to the NAP EC.</span></span>
3.  <span data-ttu-id="091c5-113">El NAP EC pasa el SoH a NAP.</span><span class="sxs-lookup"><span data-stu-id="091c5-113">The NAP EC passes the SoH to the NAP ES.</span></span>
4.  <span data-ttu-id="091c5-114">NAP ES el que pasa el SoH al servidor de administración de NAP.</span><span class="sxs-lookup"><span data-stu-id="091c5-114">The NAP ES passes the SoH to the NAP Administration Server.</span></span>
5.  <span data-ttu-id="091c5-115">El servidor de administración de NAP pasa el SoH al SHV.</span><span class="sxs-lookup"><span data-stu-id="091c5-115">The NAP Administration Server passes the SoH to the SHV.</span></span>

<span data-ttu-id="091c5-116">En la siguiente ilustración se muestra el proceso de comunicación de los componentes del cliente de NAP a los componentes del lado servidor NAP.</span><span class="sxs-lookup"><span data-stu-id="091c5-116">The figure below shows the communication process from NAP client components to NAP server-side components.</span></span>

![arquitectura de la comunicación de cliente a servidor en la plataforma NAP](images/nap-client-to-server-comm.png)

<span data-ttu-id="091c5-118">El servidor de administración de NAP puede comunicarse con el agente NAP a través del proceso siguiente:</span><span class="sxs-lookup"><span data-stu-id="091c5-118">The NAP Administration Server can communicate with the NAP Agent through the following process:</span></span>

1.  <span data-ttu-id="091c5-119">El servidor de administración de NAP pasa el SoHRs al servicio NPS.</span><span class="sxs-lookup"><span data-stu-id="091c5-119">The NAP Administration Server passes the SoHRs to the NPS service.</span></span>
2.  <span data-ttu-id="091c5-120">El servicio NPS pasa el SSoHR a NAP ES.</span><span class="sxs-lookup"><span data-stu-id="091c5-120">The NPS service passes the SSoHR to the NAP ES.</span></span>
3.  <span data-ttu-id="091c5-121">NAP ES pasa el SSoHR a NAP EC.</span><span class="sxs-lookup"><span data-stu-id="091c5-121">The NAP ES passes the SSoHR to the NAP EC.</span></span>
4.  <span data-ttu-id="091c5-122">El NAP EC pasa el SSoHR al agente NAP.</span><span class="sxs-lookup"><span data-stu-id="091c5-122">The NAP EC passes the SSoHR to the NAP Agent.</span></span>

<span data-ttu-id="091c5-123">El SHV puede comunicarse con su SHA correspondiente a través del proceso siguiente:</span><span class="sxs-lookup"><span data-stu-id="091c5-123">The SHV can communicate with its corresponding SHA through the following process:</span></span>

1.  <span data-ttu-id="091c5-124">El SHV pasa su SoHR al servidor de administración de NAP.</span><span class="sxs-lookup"><span data-stu-id="091c5-124">The SHV passes its SoHR to the NAP Administration Server.</span></span>
2.  <span data-ttu-id="091c5-125">El servidor de administración de NAP pasa el SoHR al servicio NPS.</span><span class="sxs-lookup"><span data-stu-id="091c5-125">The NAP Administration Server passes the SoHR to the NPS service.</span></span>
3.  <span data-ttu-id="091c5-126">El servicio NPS pasa el SoHR, contenido dentro de SSoHR, a NAP ES.</span><span class="sxs-lookup"><span data-stu-id="091c5-126">The NPS service passes the SoHR, contained within the SSoHR, to the NAP ES.</span></span>
4.  <span data-ttu-id="091c5-127">NAP ES pasa el SoHR a NAP EC.</span><span class="sxs-lookup"><span data-stu-id="091c5-127">The NAP ES passes the SoHR to the NAP EC.</span></span>
5.  <span data-ttu-id="091c5-128">El NAP EC pasa el SoHR al agente NAP.</span><span class="sxs-lookup"><span data-stu-id="091c5-128">The NAP EC passes the SoHR to the NAP Agent.</span></span>
6.  <span data-ttu-id="091c5-129">El agente NAP pasa el SoHR al SHA.</span><span class="sxs-lookup"><span data-stu-id="091c5-129">The NAP Agent passes the SoHR to the SHA.</span></span>

<span data-ttu-id="091c5-130">En la siguiente ilustración se muestra el proceso de comunicación de los componentes del lado servidor NAP a los componentes del cliente de NAP.</span><span class="sxs-lookup"><span data-stu-id="091c5-130">The figure below shows the communication process from NAP server-side components to NAP client components.</span></span>

![arquitectura de la comunicación de servidor a cliente en la plataforma NAP](images/nap-server-to-client-comm.png)

 

 




