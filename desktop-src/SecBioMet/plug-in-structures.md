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
# <a name="plug-in-structures"></a>Estructuras de complementos

La API de Plataforma de biometría de Windows admite las siguientes estructuras para el desarrollo de aplicaciones cliente.

## <a name="in-this-section"></a>En esta sección



| Tema                                                                                                | Descripción                                                                                                                           |
|------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| [**\_Directiva de cuenta de WINBIO \_**](winbio-account-policy.md)<br/>                                  | Contiene una directiva de suplantación predeterminada o específica de la cuenta.<br/>                                                         |
| [**versión de la interfaz del adaptador de WINBIO \_ \_ \_**](/windows/desktop/api/Winbio_adapter/ns-winbio_adapter-winbio_adapter_interface_version)<br/>           | Contiene un número de versión principal y secundaria que se usa en las tablas de la interfaz del motor, el sensor y el adaptador de almacenamiento.<br/>                |
| [**\_interfaz del motor WINBIO \_**](/windows/desktop/api/Winbio_adapter/ns-winbio_adapter-winbio_engine_interface)<br/>                              | Contiene punteros a las funciones del adaptador de motor personalizado.<br/>                                                                 |
| [**WINBIO \_ \_ parámetros de inscripción extendida \_**](winbio-extended-enrollment-parameters.md)<br/> | Contiene información adicional que un adaptador de motor necesita para crear una plantilla de inscripción. <br/>                            |
| [**\_canalización WINBIO**](/windows/desktop/api/Winbio_adapter/ns-winbio_adapter-winbio_pipeline)<br/>                                               | Contiene información de contexto compartida utilizada por los componentes del adaptador de almacenamiento, motor y sensor en una única unidad biométrica.<br/> |
| [**\_interfaz del sensor de WINBIO \_**](/windows/desktop/api/Winbio_adapter/ns-winbio_adapter-winbio_sensor_interface)<br/>                              | Contiene punteros a las funciones del adaptador de sensor personalizado.<br/>                                                                 |
| [**\_interfaz de almacenamiento de WINBIO \_**](/windows/desktop/api/Winbio_adapter/ns-winbio_adapter-winbio_storage_interface)<br/>                            | Contiene punteros a las funciones del adaptador de almacenamiento personalizado.<br/>                                                                |
| [**\_registro de almacenamiento de WINBIO \_**](/windows/desktop/api/Winbio_adapter/ns-winbio_adapter-winbio_storage_record)<br/>                                  | Contiene una plantilla biométrica y datos asociados en formato estándar.<br/>                                                    |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Referencia del complemento](plug-in-reference.md)
</dt> <dt>

[Funciones de complemento](plug-in-functions.md)
</dt> <dt>

[**WbioQueryEngineInterface**](/windows/desktop/api/Winbio_adapter/nf-winbio_adapter-wbioqueryengineinterface)
</dt> <dt>

[**WbioQuerySensorInterface**](/windows/desktop/api/Winbio_adapter/nf-winbio_adapter-wbioquerysensorinterface)
</dt> <dt>

[**WbioQueryStorageInterface**](/windows/desktop/api/Winbio_adapter/nf-winbio_adapter-wbioquerystorageinterface)
</dt> </dl>

 

 





