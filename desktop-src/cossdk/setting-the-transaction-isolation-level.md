---
description: Puede establecer manualmente el nivel de aislamiento de transacción de los componentes mediante la herramienta administrativa Servicios de componentes, o bien puede configurar mediante programación el nivel de aislamiento de transacción para un componente mediante las interfaces de administración de COM+.
ms.assetid: 3ef5b805-334d-4803-be67-00c9e35cdcc6
title: Establecer el nivel de aislamiento de la transacción
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 96af7017f8a46f11428bfacf7282a7d4ae61b4dc3c1fd5bb7e82588f8fff6110
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120029465"
---
# <a name="setting-the-transaction-isolation-level"></a>Establecer el nivel de aislamiento de la transacción

Puede establecer manualmente el nivel de aislamiento de transacción de los componentes mediante la herramienta administrativa Servicios de componentes, o bien puede configurar mediante programación el nivel de aislamiento de transacción para un componente mediante las interfaces de administración [de COM+.](com--administration-interfaces.md)

Para obtener más información sobre los niveles de aislamiento de transacción, vea [Configuring Transaction Isolation Levels](configuring-transaction-isolation-levels.md).

**Para establecer el nivel de aislamiento de transacción mediante la herramienta administrativa Servicios de componentes**

1.  En el árbol de consola, haga clic con el botón derecho en el componente que desea configurar y, a continuación, haga clic en **Propiedades.**

2.  En el cuadro de diálogo Propiedades del componente, haga clic **en la pestaña** Transacciones .

3.  En **Nivel de aislamiento de** transacción, seleccione el valor que desee en el cuadro desplegable. El valor predeterminado de todos los componentes **es Serialized**.

    > [!Note]  
    > Si se **selecciona Deshabilitado** o No **compatible en** Compatibilidad con transacciones, no se puede establecer el nivel de aislamiento de transacción. 

     

4.  Haga clic en **Aceptar**.

Debe repetir este procedimiento para cada componente.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Configuración de niveles de aislamiento de transacción](configuring-transaction-isolation-levels.md)
</dt> </dl>

 

 



