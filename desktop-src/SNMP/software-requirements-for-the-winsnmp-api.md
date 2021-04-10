---
title: Requisitos de software para la API WinSNMP
description: Una aplicación WinSNMP debe tener acceso a la API WinSNMP a través de la biblioteca de vínculos dinámicos WSNMP32.DLL.
ms.assetid: ba0b9443-3fcf-41e2-993e-54e042f9d785
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e31c30302f9f6d15cef221da46ce721dc4727a44
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104268248"
---
# <a name="software-requirements-for-the-winsnmp-api"></a><span data-ttu-id="8011d-103">Requisitos de software para la API WinSNMP</span><span class="sxs-lookup"><span data-stu-id="8011d-103">Software Requirements for the WinSNMP API</span></span>

<span data-ttu-id="8011d-104">Una aplicación WinSNMP debe tener acceso a la API WinSNMP a través de la biblioteca de vínculos dinámicos WSNMP32.DLL.</span><span class="sxs-lookup"><span data-stu-id="8011d-104">A WinSNMP application must access the WinSNMP API through the dynamic-link library WSNMP32.DLL.</span></span>

<span data-ttu-id="8011d-105">Los siguientes archivos son necesarios para admitir la funcionalidad de la API WinSNMP.</span><span class="sxs-lookup"><span data-stu-id="8011d-105">The following files are required to support the functionality of the WinSNMP API.</span></span>



| <span data-ttu-id="8011d-106">Nombre de archivo</span><span class="sxs-lookup"><span data-stu-id="8011d-106">Filename</span></span>     | <span data-ttu-id="8011d-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="8011d-107">Description</span></span>                                                                                  |
|--------------|----------------------------------------------------------------------------------------------|
| <span data-ttu-id="8011d-108">WSNMP32. OBJ</span><span class="sxs-lookup"><span data-stu-id="8011d-108">WSNMP32.LIB</span></span>  | <span data-ttu-id="8011d-109">Biblioteca WinSNMP</span><span class="sxs-lookup"><span data-stu-id="8011d-109">WinSNMP Library</span></span>                                                                              |
| <span data-ttu-id="8011d-110">WSNMP32.DLL</span><span class="sxs-lookup"><span data-stu-id="8011d-110">WSNMP32.DLL</span></span>  | <span data-ttu-id="8011d-111">Proporciona la interfaz WinSNMP</span><span class="sxs-lookup"><span data-stu-id="8011d-111">Provides WinSNMP interface</span></span>                                                                   |
| <span data-ttu-id="8011d-112">WINSNMP. C</span><span class="sxs-lookup"><span data-stu-id="8011d-112">WINSNMP.H</span></span>    | <span data-ttu-id="8011d-113">Archivo de encabezado WinSNMP</span><span class="sxs-lookup"><span data-stu-id="8011d-113">WinSNMP header file</span></span>                                                                          |
| <span data-ttu-id="8011d-114">SNMPTRAP.EXE</span><span class="sxs-lookup"><span data-stu-id="8011d-114">SNMPTRAP.EXE</span></span> | <span data-ttu-id="8011d-115">Recibe capturas de SNMP y las reenvía a MGMTAPI.DLL, la biblioteca de API del administrador SNMP de Microsoft</span><span class="sxs-lookup"><span data-stu-id="8011d-115">Receives SNMP traps and forwards them to MGMTAPI.DLL, the Microsoft SNMP Manager API library</span></span> |
| <span data-ttu-id="8011d-116">SNMPAPI.DLL</span><span class="sxs-lookup"><span data-stu-id="8011d-116">SNMPAPI.DLL</span></span>  | <span data-ttu-id="8011d-117">Proporciona utilidades SNMP</span><span class="sxs-lookup"><span data-stu-id="8011d-117">Provides SNMP utilities</span></span>                                                                      |



 

 

 




