---
description: Puede usar la herramienta administrativa Servicios de componentes para importar componentes específicos de aplicaciones que ya se han registrado en el equipo como componentes COM en el registro Windows componentes.
ms.assetid: 5310e08a-5146-41f8-ae65-8467b921abd4
title: Importar componentes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 69385e14759716e775ce608307b3ef12828e5f628539e58a1d214d6c11506e66
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119953985"
---
# <a name="importing-components"></a>Importar componentes

Puede usar la herramienta administrativa Servicios de componentes para importar componentes específicos de aplicaciones que ya se han registrado en el equipo como componentes COM en el registro Windows componentes. La importación de un componente no instala la información de interfaz o método necesaria para establecer las propiedades de la interfaz ni para configurar el acceso al componente desde un cliente remoto. Por lo tanto, si es posible, debe instalar en lugar de importar componentes no configurados.

> [!Note]  
> Al importar un componente en una aplicación COM+, COM+ no rellena la información de interfaz y método del componente. Durante la exportación de un proxy de aplicación, COM+ no proporcionará información de serialización (bibliotecas de tipos o proxy/stubs) para algunas o todas las interfaces. La exportación de servidores proxy de aplicación que contienen componentes importados producirá un error o provocará que se emita una advertencia.

 

**Para importar un componente en una aplicación COM+**

1.  En el árbol de consola de la herramienta administrativa Servicios de componentes, seleccione el equipo que hospeda la aplicación COM+.

2.  Abra la **carpeta Aplicaciones COM+** para ese equipo y seleccione la aplicación en la que desea instalar el componente.

3.  Abra la carpeta de la aplicación y seleccione **Componentes**.

4.  En el **menú Acción,** seleccione **Nuevo y,** a continuación, haga clic en **Componente**. También puede hacer clic con el botón derecho en la **carpeta Componentes,** seleccionar **Nuevo** y, a continuación, hacer clic en **Componente**.

5.  En la **página** principal del Asistente para instalación de aplicaciones  COM+, haga clic en Siguiente y, a continuación, en el cuadro de diálogo Importar o instalar un componente , haga clic en Importar componentes que ya están **registrados.**

6.  En el cuadro de diálogo Elegir  componentes **para** importar, active la casilla Detalles para ver información completa sobre los componentes que ya están registrados. Seleccione los componentes que desea importar de la lista mostrada y haga clic en **Siguiente.**

7.  Haga clic en **Finalizar**

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Copiar componentes](copying-components.md)
</dt> <dt>

[Creación de una nueva aplicación COM+](creating-a-new-com--application.md)
</dt> <dt>

[Eliminación de una aplicación COM+](deleting-a-com--application.md)
</dt> <dt>

[Instalación de nuevos componentes](installing-new-components.md)
</dt> <dt>

[Mover componentes](moving-components.md)
</dt> <dt>

[Quitar un componente de una aplicación COM+](removing-a-component-from-a-com--application.md)
</dt> </dl>

 

 



