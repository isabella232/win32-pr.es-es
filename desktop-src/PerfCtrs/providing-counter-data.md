---
description: En Windows Vista, los contadores de rendimiento implementaron una nueva arquitectura (versión 2,0) para proporcionar los datos del contador.
ms.assetid: c17eda2f-3cf8-40d6-8be6-c1ce190d1a26
title: Proporcionar datos de contador
ms.topic: article
ms.date: 08/17/2020
ms.openlocfilehash: ed5aa4cc505baab9e15d3f69c3fb466712eddbfe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105667254"
---
# <a name="providing-counter-data"></a>Proporcionar datos de contador

Los componentes de software que publican datos mediante los contadores de rendimiento de Windows se denominan proveedores de datos de rendimiento.

Windows admite dos tipos de proveedores de datos de rendimiento. Los proveedores de datos de rendimiento heredados (**proveedores v1**) se implementan mediante. Archivo INI y un archivo DLL de rendimiento. Los proveedores de datos de rendimiento modernos (**proveedores V2**) usan un. MAN (manifiesto XML) y las API del proveedor de contadores de rendimiento.

## <a name="manifests"></a>Manifiestos

Los proveedores de datos de rendimiento modernos usan un. MAN (manifiesto XML) para definir los datos del contador y usar las API del proveedor de contadores de rendimiento para administrar los datos en el contexto del proveedor.

Los proveedores implementados mediante un manifiesto y las API de proveedor de contadores de rendimiento a menudo se denominan **proveedores V2**.

Windows admite proveedores de modo usuario V2 en Windows Vista o posterior. Para obtener detalles sobre el modo de usuario, consulte [proporcionar datos de contadores con la versión 2,0](providing-counter-data-using-version-2-0.md).

Windows admite proveedores de modo kernel v2 en Windows 7 o posterior. Para obtener detalles sobre el modo kernel, consulte [supervisión del rendimiento del modo kernel](/windows-hardware/drivers/devtest/kernel-mode-performance-monitoring).

## <a name="performance-dll-deprecated"></a>DLL de rendimiento (desusado)

En la arquitectura del contador de rendimiento heredado, los proveedores implementaron un archivo DLL de rendimiento en que se ejecutaba en el proceso del consumidor para recopilar y proporcionar los datos del contador cuando un consumidor lo solicitó. El proveedor usó una inicialización (. INI) y entradas del registro para definir los contadores y configurar el archivo DLL de rendimiento.

Proveedores implementados mediante. El archivo INI y un archivo DLL de rendimiento a menudo se denominan **proveedores v1**.

> [!CAUTION]
> Aunque todavía puede usar un archivo DLL de rendimiento para proporcionar datos de contador, esta arquitectura está en desuso debido a las limitaciones de rendimiento y confiabilidad significativas. Además, los proveedores v1 suelen ser más difíciles de implementar, ya que requieren el envío de un archivo DLL independiente que deba ejecutarse en el proceso del consumidor.

Para obtener más información, vea [proporcionar datos de contador mediante un archivo dll de rendimiento](providing-counter-data-using-a-performance-dll.md).
