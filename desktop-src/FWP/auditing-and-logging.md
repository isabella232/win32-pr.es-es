---
title: Auditoría
description: Windows La plataforma de filtrado (WFP) proporciona auditoría de eventos relacionados con el firewall y IPsec.
ms.assetid: 30ff9cf7-bf93-4979-bacd-d76e5dadbef6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 62e62995cfe227bc31897e6a5ca73fc09c780ce7
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2021
ms.locfileid: "122483061"
---
# <a name="auditing"></a>Auditoría

La plataforma Windows filtrado de datos (WFP) proporciona auditoría de eventos relacionados con el firewall y IPsec. Estos eventos se almacenan en el registro de seguridad del sistema.

Los eventos auditados son los siguientes.




| Categoría auditoría | Subcategoría de auditoría | Eventos auditados | 
|-------------------|----------------------|----------------|
| Cambio de directiva<br /> {6997984D-797A-11D9-BED3-505054503030}<br /> | Filtrado del cambio de directiva de plataforma<br /> {0CCE9233-69AE-11D9-BED3-505054503030}<br /> | <blockquote>[!Note]<br />Los números representan los valores de Event ID como se muestra Visor de eventos (eventvwr.exe).</blockquote><br /> Adición y eliminación de objetos WFP:<br /><ul><li>5440 Llamada persistente agregada</li><li>5441 Tiempo de arranque o filtro persistente agregado</li><li>Se ha agregado el proveedor persistente 5442.</li><li>5443 Contexto de proveedor persistente agregado</li><li>5444 Subcapa persistente agregada</li><li>5446 Llamada en tiempo de ejecución agregada o eliminada</li><li>5447 Filtro en tiempo de ejecución agregado o quitado</li><li>5448 Proveedor en tiempo de ejecución agregado o quitado</li><li>5449 Contexto de proveedor en tiempo de ejecución agregado o quitado</li><li>5450 Subcapa en tiempo de ejecución agregada o quitada</li></ul> | 
| Acceso a objetos<br /> {6997984A-797A-11D9-BED3-505054503030}<br /> | Filtrado de la colocación de paquetes de plataforma <br /> {0CCE9225-69AE-11D9-BED3-505054503030}<br /> | Paquetes descartados por WFP:<br /><ul><li>5152 Paquete eliminado</li><li>5153 Paquete veto</li></ul> | 
| Acceso a objetos<br /> | Filtrado de la conexión de plataforma <br /> {0CCE9226-69AE-11D9-BED3-505054503030}<br /> | Conexiones permitidas y bloqueadas:<br /><ul><li>5154 Escucha permitida</li><li>5155 Escucha bloqueada</li><li>5156 Conexión permitida</li><li>5157 Conexión bloqueada</li><li>5158 Enlace permitido</li><li>5159 Enlace bloqueado</li></ul><blockquote>[!Note]<br />Las conexiones permitidas no siempre auditan el identificador del filtro asociado. FilterID para TCP será 0 a menos que se utilice un subconjunto de estas condiciones de filtrado: UserID, AppID, Protocol y Remote Port.</blockquote><br /> | 
| Acceso a objetos<br /> | Otros eventos de acceso a objetos<br /> {0CCE9227-69AE-11D9-BED3-505054503030}<br /> | <blockquote>[!Note]<br />Esta subcategoría permite muchas auditorías. A continuación se enumeran las auditorías específicas de WFP.</blockquote><br /> Estado de prevención de denegación de servicio:<br /><ul><li>5148 Se inició el modo de prevención de doS de WFP</li><li>5149 Modo de prevención de doS de WFP detenido</li></ul> | 
| Inicio/cierre de sesión<br /> {69979849-797A-11D9-BED3-505054503030}<br /> | Modo principal de IPsec<br /> {0CCE9218-69AE-11D9-BED3-505054503030}<br /> | Negociación del modo principal de IKE y AuthIP:<br /><ul><li>4650, 4651 Asociación de seguridad establecida</li><li>4652, 4653 Error de negociación</li><li>4655 La asociación de seguridad finalizó</li></ul> | 
| Inicio/cierre de sesión<br /> | Modo rápido de IPsec <br /> {0CCE9219-69AE-11D9-BED3-505054503030}<br /> | Negociación del modo rápido de IKE y AuthIP:<br /><ul><li>5451 Asociación de seguridad establecida</li><li>5452 La asociación de seguridad finalizó</li><li>4654 Error de negociación</li></ul> | 
| Inicio/cierre de sesión <br /> | Modo extendido de IPsec<br /> {0CCE921A-69AE-11D9-BED3-505054503030}<br /> | Negociación del modo extendido de AuthIP:<br /><ul><li>4978 Paquete de negociación no válido</li><li>4979, 4980, 4981, 4982 Asociación de seguridad establecida</li><li>4983, 4984 Error de negociación</li></ul> | 
| Sistema<br /> {69979848-797A-11D9-BED3-505054503030}<br /> | Controlador IPsec<br /> {0CCE9213-69AE-11D9-BED3-505054503030}<br /> | Paquetes descartados por el controlador IPsec:<br /><ul><li>4963 Paquete de texto no enviado entrante eliminado</li></ul> | 




 

De forma predeterminada, la auditoría de WFP está deshabilitada.

La auditoría se puede habilitar por categoría mediante el complemento MMC de Editor de objetos de directiva de grupo, el complemento MMC de directiva de seguridad local o el comando auditpol.exe.

Por ejemplo, para habilitar la auditoría de eventos de cambio de directiva, puede hacer lo siguiente:

-   Use el Editor de objetos de directiva de grupo

    1.  Ejecute **gpedit.msc.**
    2.  Expanda Directiva de equipo local.
    3.  Expanda Configuración del equipo.
    4.  Expanda Windows Configuración.
    5.  Expanda Seguridad Configuración.
    6.  Expanda Directivas locales.
    7.  Haz clic en Directiva de auditoría.
    8.  Haga doble clic en Auditar cambio de directiva para iniciar el cuadro de diálogo Propiedades.
    9.  Active las casillas Correcto y Error.

-   Uso de la directiva de seguridad local

    1.  Ejecute **secpol.msc.**
    2.  Expanda Directivas locales.
    3.  Haz clic en Directiva de auditoría.
    4.  Haga doble clic en Auditar cambio de directiva para iniciar el cuadro de diálogo Propiedades.
    5.  Active las casillas Correcto y Error.

-   Uso del auditpol.exe comando

    -   **auditpol /set /category:"Policy Change" /success:enable /failure:enable**

La auditoría solo se puede habilitar por subcategoría a través del auditpol.exe aplicación.

Los nombres de categoría y subcategoría de auditoría están localizados. Para evitar la localización de scripts de auditoría, se pueden usar los GUID correspondientes en lugar de los nombres.

Por ejemplo, para habilitar la auditoría de eventos de cambio de directiva de plataforma de filtrado, puede usar cualquiera de los siguientes comandos:

-   **auditpol /set /subcategory:"Filtering Platform Policy Change" /success:enable /failure:enable**
-   **auditpol /set /subcategory:"{0CCE9233-69AE-11D9-BED3-505054503030}" /success:enable /failure:enable**

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Auditpol](/previous-versions/windows/it-pro/windows-server-2012-R2-and-2012/cc731451(v=ws.11))
</dt> <dt>

[Registro de eventos](/previous-versions/orphan-topics/ws.10/dd996684(v=ws.10))
</dt> <dt>

[Directiva de grupo](/windows/deployment/deploy-whats-new)
</dt> </dl>

