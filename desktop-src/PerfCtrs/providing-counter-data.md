---
description: En Windows Vista, los contadores de rendimiento implementaron una nueva arquitectura (versión 2.0) para proporcionar datos de contador.
ms.assetid: c17eda2f-3cf8-40d6-8be6-c1ce190d1a26
title: Proporcionar datos de contador
ms.topic: article
ms.date: 08/17/2020
ms.openlocfilehash: 0a17a6c75a86a7ee86f26350b9ea7680f0ba08338dbe7dc18cd56a8c425ba3ba
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117793628"
---
# <a name="providing-counter-data"></a>Proporcionar datos de contador

Los componentes de software que publican datos a través Windows contadores de rendimiento se denominan proveedores de datos de rendimiento.

Windows admite dos tipos de proveedores de datos de rendimiento. Los proveedores de datos de rendimiento heredados **(proveedores V1)** se implementan mediante un archivo .INI y un archivo DLL de rendimiento. Los proveedores de datos de rendimiento modernos **(proveedores V2)** usan . MAN (manifiesto XML) y las API del proveedor de contadores de rendimiento.

## <a name="manifests"></a>Manifiestos

Los proveedores de datos de rendimiento moderno usan . MAN (manifiesto XML) para definir los datos del contador y usar las API del proveedor de contadores de rendimiento para administrar los datos en el contexto del proveedor.

Los proveedores implementados mediante un manifiesto y las API de proveedor de contadores de rendimiento a menudo se denominan **proveedores V2.**

Windows admite proveedores de modo de usuario V2 en Windows Vista o versiones posteriores. Para obtener más información sobre el modo de usuario, vea [Proporcionar datos de contador mediante la versión 2.0.](providing-counter-data-using-version-2-0.md)

Windows admite proveedores de modo kernel V2 en Windows 7 o posterior. Para obtener más información sobre el modo kernel, consulte Kernel Mode Performance Monitoring ( Supervisión del rendimiento [del modo kernel).](/windows-hardware/drivers/devtest/kernel-mode-performance-monitoring)

## <a name="performance-dll-deprecated"></a>DLL de rendimiento (en desuso)

En la arquitectura de contador de rendimiento heredada, los proveedores implementaron un archivo DLL de rendimiento en que se ejecutó en el proceso del consumidor para recopilar y proporcionar los datos del contador cuando un consumidor lo solicitó. El proveedor usó un archivo de inicialización (.INI) y entradas del Registro para definir los contadores y configurar el archivo DLL de rendimiento.

Los proveedores implementados mediante un archivo .INI y un archivo DLL de rendimiento a menudo se denominan **proveedores V1.**

> [!CAUTION]
> Aunque todavía puede usar un archivo DLL de rendimiento para proporcionar datos de contador, esta arquitectura está en desuso debido a importantes limitaciones de rendimiento y confiabilidad. Además, los proveedores de V1 suelen ser más difíciles de implementar, ya que requieren el envío de un archivo DLL independiente que se debe ejecutar en el proceso del consumidor.

Para obtener más información, vea [Proporcionar datos de contador mediante un archivo DLL de rendimiento.](providing-counter-data-using-a-performance-dll.md)
