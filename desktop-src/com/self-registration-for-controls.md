---
title: Registro propio para controles
description: Registro propio para controles
ms.assetid: 0fff07e5-10bb-4052-8eb1-021efcb66d6c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bfdf2d71dcee1727031dd6ad9d55d88baf86a6b3
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/21/2020
ms.locfileid: "105695768"
---
# <a name="self-registration-for-controls"></a>Registro propio para controles

Los controles ActiveX deben admitir el registro automático mediante la implementación de las funciones [**DllRegisterServer**](/windows/win32/api/olectl/nf-olectl-dllregisterserver) y [**DllUnregisterServer**](/windows/win32/api/olectl/nf-olectl-dllunregisterserver) . Los controles ActiveX deben registrar todas las entradas del registro estándar para los objetos incrustables y los servidores de automatización.

Los controles ActiveX deben usar la API de categorías de componentes para registrarse como control y registrar las categorías de componentes que requieren que un host admita y las categorías que el control implementa, vea [categorías de componentes](component-categories.md).

Los controles ActiveX también deben registrar la clave del registro [ToolBoxBitmap32](toolboxbitmap32.md) , aunque esto no es obligatorio.

La categoría de componente insertable solo debe registrarse si el control es adecuado para su uso como un objeto de documento compuesto. Es importante tener en cuenta que un objeto de documento compuesto debe admitir ciertas interfaces más allá del valor [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) mínimo necesario para un control ActiveX. Aunque un control ActiveX puede calificarse como un objeto de documento compuesto, la documentación del control debe indicar claramente qué comportamiento esperar en estas circunstancias.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Controles](controls.md)
</dt> </dl>

 

 