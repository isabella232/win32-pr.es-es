---
description: Los valores de sincronización se pueden determinar o restringir automáticamente mediante la configuración de otras propiedades, como los requisitos transaccionales y la activación Just-In-Time (JIT).
ms.assetid: 16771121-cb10-42b4-babc-59270188495a
title: Dependencias de sincronización
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c139d0d6e78288b25e42bd0a84b29432cebb44ca
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127361629"
---
# <a name="synchronization-dependencies"></a>Dependencias de sincronización

Los valores de sincronización se pueden determinar o restringir automáticamente mediante la configuración de otras propiedades, como los requisitos transaccionales y la activación Just-In-Time (JIT). Por ejemplo, COM+ aplica la sincronización tanto para los componentes transaccionales como para los componentes activados por JIT.

Estas dependencias existen porque los componentes que están activados por JIT o que participan en transacciones deben tener el aislamiento y el comportamiento de simultaneidad adecuados. Por lo tanto, COM+ requiere que el acceso a estos componentes se serializó mediante la aplicación de la sincronización. (Para obtener más información sobre estas dependencias, [vea Activación Just-In-Time de COM+).](com--just-in-time-activation.md)

En las tablas siguientes se muestran las características de los valores de atributo de sincronización de COM+.

### <a name="transactional-requirement"></a>Requisito transaccional



| Cuando las transacciones se establecen en | La sincronización se puede establecer en                    |
|------------------------------|--------------------------------------------------|
| Disabled<br/>          | Cualquier cosa, en función de la activación JIT<br/> |
| No compatible<br/>     | Cualquier cosa, en función de la activación JIT<br/> |
| Compatible<br/>         | Obligatorio<br/>                              |
| Obligatorio<br/>          | Obligatorio<br/>                              |
| Se requiere nueva<br/>      | Requerido o requiere nuevo<br/>              |



 

### <a name="jit-activation"></a>Activación JIT



| Cuando la activación JIT está establecida en | La sincronización se puede establecer en       |
|-------------------------------|-------------------------------------|
| habilitado<br/>            | Requerido o requiere nuevo<br/> |
| Disabled<br/>           | Nada<br/>                 |



 

Para obtener más información sobre cómo se comportan conjuntamente los atributos de transacción, activación JIT y sincronización, vea [Configuring Transactions](configuring-transactions.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Establecer el atributo de sincronización](setting-the-synchronization-attribute.md)
</dt> <dt>

[Valores de atributo de sincronización](synchronization-attribute-values.md)
</dt> </dl>

 

 




