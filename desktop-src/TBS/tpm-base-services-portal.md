---
title: Servicios base de TPM
description: El software TPM proporciona servicios como una API expuesta a través de la llamada a procedimiento remoto. Use TPM para crear un módulo de TPM.
ms.assetid: ae6e7fe9-585d-467a-8456-e008b8ea89a0
keywords:
- Servicios base de TPM TBS
- Servicios base de TPM TBS, Página principal
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9d2cbdfc1f85d6917f2e9a7a5b8e7a0fc25ebdc8
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104421079"
---
# <a name="tpm-base-services"></a>Servicios base de TPM

## <a name="purpose"></a>Propósito

La característica de servicios base de Módulo de plataforma segura (TBS) centraliza el acceso de TPM entre las aplicaciones.

La característica TBS se ejecuta como un servicio de sistema en Windows Server 2008, Windows Vista o sistemas operativos más recientes. Proporciona servicios como una API expuesta a través de llamadas a procedimiento remoto (RPC). La característica TBS usa las prioridades especificadas al llamar a las aplicaciones para programar el acceso de TPM de forma cooperativa.

> [!Note]
>
> El TPM se puede usar para las operaciones de almacenamiento de claves. Sin embargo, se recomienda que los desarrolladores usen las [API de almacenamiento de claves](/windows/desktop/SecCNG/key-storage-and-retrieval) para estos escenarios en su lugar. Las API de almacenamiento de claves proporcionan la funcionalidad para crear, firmar o cifrar con y conservar claves criptográficas, y son de mayor nivel y más fáciles de usar que los TBS para estos escenarios de destino.

 

## <a name="developer-audience"></a>Audiencia de desarrolladores

TBS está pensado para que lo usen los desarrolladores de aplicaciones basadas en los sistemas operativos Windows. Los desarrolladores deben estar familiarizados con los lenguajes de programación C y C++ y el entorno de programación de Microsoft Windows.

## <a name="run-time-requirements"></a>Requisitos de tiempo de ejecución

La característica TBS requiere como mínimo el sistema operativo Windows Server 2008 o Windows Vista. Para obtener información sobre los requisitos de tiempo de ejecución para un elemento de programación determinado, vea la sección de requisitos de la página de referencia de ese elemento.

## <a name="in-this-section"></a>En esta sección



| Tema                                         | Descripción                                                                     |
|-----------------------------------------------|---------------------------------------------------------------------------------|
| [Acerca de TBS](about-tbs.md)<br/>         | Conceptos clave y una vista de alto nivel de la característica de TBS.<br/>               |
| [Uso de TBS](using-tbs.md)<br/>         | Procesos y procedimientos de TBS para usar la API de TBS.<br/>                  |
| [Referencia de TBS](tbs-reference.md)<br/> | Documentación acerca de las funciones, estructuras y códigos de retorno de TBS.<br/> |



 

 

