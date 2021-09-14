---
title: Servicios base de TPM
description: El software tpm proporciona servicios como una API expuesta a través de una llamada a procedimiento remoto. Use TPM para crear un módulo de TPM.
ms.assetid: ae6e7fe9-585d-467a-8456-e008b8ea89a0
keywords:
- TBS de servicios base de TPM
- TPM Base Services TBS, página principal
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9d2cbdfc1f85d6917f2e9a7a5b8e7a0fc25ebdc8
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127243764"
---
# <a name="tpm-base-services"></a>Servicios base de TPM

## <a name="purpose"></a>Propósito

La característica Módulo de plataforma segura base de tpm (TPM) centraliza el acceso de TPM entre aplicaciones.

La característica TBS se ejecuta como un servicio del sistema en Windows Server 2008, Windows Vista o sistemas operativos más recientes. Proporciona servicios como una API expuesta a través de llamadas a procedimiento remoto (RPC). La característica TBS usa prioridades especificadas mediante una llamada a las aplicaciones para programar de forma cooperativa el acceso a TPM.

> [!Note]
>
> El TPM se puede usar para las operaciones de almacenamiento de claves. Sin embargo, se recomienda a los desarrolladores que usen key [Storage API](/windows/desktop/SecCNG/key-storage-and-retrieval) para estos escenarios en su lugar. Las API de key Storage proporcionan la funcionalidad para crear, firmar o cifrar con y conservar claves criptográficas, y son de nivel superior y más fáciles de usar que los TBS para estos escenarios de destino.

 

## <a name="developer-audience"></a>Audiencia de desarrolladores

TBS está pensado para su uso por parte de los desarrolladores de aplicaciones basadas en Windows sistemas operativos. Los desarrolladores deben estar familiarizados con los lenguajes de programación C y C++ y el entorno de programación Windows Microsoft.

## <a name="run-time-requirements"></a>Requisitos de tiempo de ejecución

La característica TBS requiere al menos Windows Server 2008 o Windows operativo Vista. Para obtener información sobre los requisitos en tiempo de ejecución para un elemento de programación determinado, vea la sección Requisitos de la página de referencia de ese elemento.

## <a name="in-this-section"></a>En esta sección



| Tema                                         | Descripción                                                                     |
|-----------------------------------------------|---------------------------------------------------------------------------------|
| [Acerca de TBS](about-tbs.md)<br/>         | Conceptos clave y una vista de alto nivel de la característica TBS.<br/>               |
| [Uso de TBS](using-tbs.md)<br/>         | Procesos y procedimientos de TBS para usar la API de TBS.<br/>                  |
| [Referencia de TBS](tbs-reference.md)<br/> | Documentación sobre las funciones, estructuras y códigos de retorno de TBS.<br/> |



 

 

