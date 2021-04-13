---
title: Estructuras de complementos
description: Estructuras para el desarrollo de aplicaciones cliente mediante la API de Plataforma de biometría de Windows.
ms.assetid: 64fb908c-72c2-4639-a2f6-77ede080512c
keywords:
- Plataforma de biometría de Windows API Plataforma de biometría de Windows API, estructuras de complementos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 193b5a99f30c76e8e6e2ab7ebf0242cf56905816
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104357521"
---
# <a name="plug-in-structures"></a><span data-ttu-id="764a6-104">Estructuras de complementos</span><span class="sxs-lookup"><span data-stu-id="764a6-104">Plug-in Structures</span></span>

<span data-ttu-id="764a6-105">La API de Plataforma de biometría de Windows admite las siguientes estructuras para el desarrollo de aplicaciones cliente.</span><span class="sxs-lookup"><span data-stu-id="764a6-105">The following structures are supported for client application development by the Windows Biometric Framework API.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="764a6-106">En esta sección</span><span class="sxs-lookup"><span data-stu-id="764a6-106">In this section</span></span>



| <span data-ttu-id="764a6-107">Tema</span><span class="sxs-lookup"><span data-stu-id="764a6-107">Topic</span></span>                                                                                                | <span data-ttu-id="764a6-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="764a6-108">Description</span></span>                                                                                                                           |
|------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="764a6-109">**\_Directiva de cuenta de WINBIO \_**</span><span class="sxs-lookup"><span data-stu-id="764a6-109">**WINBIO\_ACCOUNT\_POLICY**</span></span>](winbio-account-policy.md)<br/>                                  | <span data-ttu-id="764a6-110">Contiene una directiva de suplantación predeterminada o específica de la cuenta.</span><span class="sxs-lookup"><span data-stu-id="764a6-110">Contains either a default or account-specific antispoofing policy.</span></span><br/>                                                         |
| [<span data-ttu-id="764a6-111">**versión de la interfaz del adaptador de WINBIO \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="764a6-111">**WINBIO\_ADAPTER\_INTERFACE\_VERSION**</span></span>](/windows/desktop/api/Winbio_adapter/ns-winbio_adapter-winbio_adapter_interface_version)<br/>           | <span data-ttu-id="764a6-112">Contiene un número de versión principal y secundaria que se usa en las tablas de la interfaz del motor, el sensor y el adaptador de almacenamiento.</span><span class="sxs-lookup"><span data-stu-id="764a6-112">Contains a major and minor version number used in the engine, sensor, and storage adapter interface tables.</span></span><br/>                |
| [<span data-ttu-id="764a6-113">**\_interfaz del motor WINBIO \_**</span><span class="sxs-lookup"><span data-stu-id="764a6-113">**WINBIO\_ENGINE\_INTERFACE**</span></span>](/windows/desktop/api/Winbio_adapter/ns-winbio_adapter-winbio_engine_interface)<br/>                              | <span data-ttu-id="764a6-114">Contiene punteros a las funciones del adaptador de motor personalizado.</span><span class="sxs-lookup"><span data-stu-id="764a6-114">Contains pointers to your custom engine adapter functions.</span></span><br/>                                                                 |
| [<span data-ttu-id="764a6-115">**WINBIO \_ \_ parámetros de inscripción extendida \_**</span><span class="sxs-lookup"><span data-stu-id="764a6-115">**WINBIO\_EXTENDED\_ENROLLMENT\_PARAMETERS**</span></span>](winbio-extended-enrollment-parameters.md)<br/> | <span data-ttu-id="764a6-116">Contiene información adicional que un adaptador de motor necesita para crear una plantilla de inscripción.</span><span class="sxs-lookup"><span data-stu-id="764a6-116">Contains additional information that an engine adapter needs to create an enrollment template.</span></span> <br/>                            |
| [<span data-ttu-id="764a6-117">**\_canalización WINBIO**</span><span class="sxs-lookup"><span data-stu-id="764a6-117">**WINBIO\_PIPELINE**</span></span>](/windows/desktop/api/Winbio_adapter/ns-winbio_adapter-winbio_pipeline)<br/>                                               | <span data-ttu-id="764a6-118">Contiene información de contexto compartida utilizada por los componentes del adaptador de almacenamiento, motor y sensor en una única unidad biométrica.</span><span class="sxs-lookup"><span data-stu-id="764a6-118">Contains shared context information used by the sensor, engine, and storage adapter components in a single biometric unit.</span></span><br/> |
| [<span data-ttu-id="764a6-119">**\_interfaz del sensor de WINBIO \_**</span><span class="sxs-lookup"><span data-stu-id="764a6-119">**WINBIO\_SENSOR\_INTERFACE**</span></span>](/windows/desktop/api/Winbio_adapter/ns-winbio_adapter-winbio_sensor_interface)<br/>                              | <span data-ttu-id="764a6-120">Contiene punteros a las funciones del adaptador de sensor personalizado.</span><span class="sxs-lookup"><span data-stu-id="764a6-120">Contains pointers to your custom sensor adapter functions.</span></span><br/>                                                                 |
| [<span data-ttu-id="764a6-121">**\_interfaz de almacenamiento de WINBIO \_**</span><span class="sxs-lookup"><span data-stu-id="764a6-121">**WINBIO\_STORAGE\_INTERFACE**</span></span>](/windows/desktop/api/Winbio_adapter/ns-winbio_adapter-winbio_storage_interface)<br/>                            | <span data-ttu-id="764a6-122">Contiene punteros a las funciones del adaptador de almacenamiento personalizado.</span><span class="sxs-lookup"><span data-stu-id="764a6-122">Contains pointers to your custom storage adapter functions.</span></span><br/>                                                                |
| [<span data-ttu-id="764a6-123">**\_registro de almacenamiento de WINBIO \_**</span><span class="sxs-lookup"><span data-stu-id="764a6-123">**WINBIO\_STORAGE\_RECORD**</span></span>](/windows/desktop/api/Winbio_adapter/ns-winbio_adapter-winbio_storage_record)<br/>                                  | <span data-ttu-id="764a6-124">Contiene una plantilla biométrica y datos asociados en formato estándar.</span><span class="sxs-lookup"><span data-stu-id="764a6-124">Contains a biometric template and associated data in a standard format.</span></span><br/>                                                    |



 

## <a name="related-topics"></a><span data-ttu-id="764a6-125">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="764a6-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="764a6-126">Referencia del complemento</span><span class="sxs-lookup"><span data-stu-id="764a6-126">Plug-in Reference</span></span>](plug-in-reference.md)
</dt> <dt>

[<span data-ttu-id="764a6-127">Funciones de complemento</span><span class="sxs-lookup"><span data-stu-id="764a6-127">Plug-in Functions</span></span>](plug-in-functions.md)
</dt> <dt>

[<span data-ttu-id="764a6-128">**WbioQueryEngineInterface**</span><span class="sxs-lookup"><span data-stu-id="764a6-128">**WbioQueryEngineInterface**</span></span>](/windows/desktop/api/Winbio_adapter/nf-winbio_adapter-wbioqueryengineinterface)
</dt> <dt>

[<span data-ttu-id="764a6-129">**WbioQuerySensorInterface**</span><span class="sxs-lookup"><span data-stu-id="764a6-129">**WbioQuerySensorInterface**</span></span>](/windows/desktop/api/Winbio_adapter/nf-winbio_adapter-wbioquerysensorinterface)
</dt> <dt>

[<span data-ttu-id="764a6-130">**WbioQueryStorageInterface**</span><span class="sxs-lookup"><span data-stu-id="764a6-130">**WbioQueryStorageInterface**</span></span>](/windows/desktop/api/Winbio_adapter/nf-winbio_adapter-wbioquerystorageinterface)
</dt> </dl>

 

 





