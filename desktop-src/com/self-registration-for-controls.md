---
title: Registro propio para controles
description: Registro propio para controles
ms.assetid: 0fff07e5-10bb-4052-8eb1-021efcb66d6c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bfdf2d71dcee1727031dd6ad9d55d88baf86a6b3
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127063904"
---
# <a name="self-registration-for-controls"></a>Registro propio para controles

ActiveX controles deben admitir el registro propio mediante la implementación de las funciones [**DllRegisterServer**](/windows/win32/api/olectl/nf-olectl-dllregisterserver) y [**DllUnregisterServer.**](/windows/win32/api/olectl/nf-olectl-dllunregisterserver) ActiveX controles deben registrar todas las entradas estándar del Registro para los objetos que se pueden insertar y los servidores de automatización.

ActiveX controles deben usar la API de categorías de componentes para registrarse como un control y registrar las categorías de componentes que requieren un host para admitir y las categorías que implementa el control, consulte Categorías [de componentes](component-categories.md).

ActiveX controles también deben registrar la clave del Registro [ToolBoxBitmap32,](toolboxbitmap32.md) aunque esto no es obligatorio.

La categoría componente insertable solo debe registrarse si el control es adecuado para su uso como un objeto de documento compuesto. Es importante tener en cuenta que un objeto de documento compuesto debe admitir determinadas interfaces más allá del [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) mínimo necesario para un control ActiveX datos. Aunque un control ActiveX puede calificarse como un objeto de documento compuesto, la documentación del control debe decir claramente qué comportamiento esperar en estas circunstancias.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Controles](controls.md)
</dt> </dl>

 

 