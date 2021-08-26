---
title: Estructuras de complemento
description: Estructuras para el desarrollo de aplicaciones cliente mediante Windows Biometric Framework API.
ms.assetid: 64fb908c-72c2-4639-a2f6-77ede080512c
keywords:
- Windows API de Marco biométrico Windows API de Marco biométrico, estructuras de complemento
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e150dd043a8c95e91d0f9095e23584544f43a503a709ae54c9180e06aa40bdaf
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120101245"
---
# <a name="plug-in-structures"></a>Estructuras de complemento

Las siguientes estructuras son compatibles con el desarrollo de aplicaciones cliente mediante Windows Biometric Framework API.

## <a name="in-this-section"></a>En esta sección



| Tema                                                                                                | Descripción                                                                                                                           |
|------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| [**DIRECTIVA DE \_ CUENTA DE \_ WINBIO**](winbio-account-policy.md)<br/>                                  | Contiene una directiva de antispoofing predeterminada o específica de la cuenta.<br/>                                                         |
| [**VERSIÓN DE LA \_ INTERFAZ DEL ADAPTADOR DE \_ \_ WINBIO**](/windows/desktop/api/Winbio_adapter/ns-winbio_adapter-winbio_adapter_interface_version)<br/>           | Contiene un número de versión principal y secundaria que se usa en las tablas de interfaz del adaptador de almacenamiento, sensor y motor.<br/>                |
| [**INTERFAZ DEL \_ MOTOR \_ WINBIO**](/windows/desktop/api/Winbio_adapter/ns-winbio_adapter-winbio_engine_interface)<br/>                              | Contiene punteros a las funciones del adaptador de motor personalizadas.<br/>                                                                 |
| [**PARÁMETROS DE INSCRIPCIÓN EXTENDIDA DE WINBIO \_ \_ \_**](winbio-extended-enrollment-parameters.md)<br/> | Contiene información adicional que un adaptador de motor necesita para crear una plantilla de inscripción. <br/>                            |
| [**CANALIZACIÓN DE \_ WINBIO**](/windows/desktop/api/Winbio_adapter/ns-winbio_adapter-winbio_pipeline)<br/>                                               | Contiene información de contexto compartido utilizada por los componentes del sensor, el motor y el adaptador de almacenamiento en una sola unidad biométrica.<br/> |
| [**INTERFAZ DEL \_ SENSOR \_ WINBIO**](/windows/desktop/api/Winbio_adapter/ns-winbio_adapter-winbio_sensor_interface)<br/>                              | Contiene punteros a las funciones de adaptador de sensor personalizadas.<br/>                                                                 |
| [**INTERFAZ DE \_ ALMACENAMIENTO DE \_ WINBIO**](/windows/desktop/api/Winbio_adapter/ns-winbio_adapter-winbio_storage_interface)<br/>                            | Contiene punteros a las funciones de adaptador de almacenamiento personalizadas.<br/>                                                                |
| [**REGISTRO DE \_ ALMACENAMIENTO \_ WINBIO**](/windows/desktop/api/Winbio_adapter/ns-winbio_adapter-winbio_storage_record)<br/>                                  | Contiene una plantilla biométrica y los datos asociados en un formato estándar.<br/>                                                    |



 

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

 

 





