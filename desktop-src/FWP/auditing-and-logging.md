---
title: Auditoría
description: Windows La plataforma de filtrado (WFP) proporciona auditoría de eventos relacionados con el firewall y IPsec.
ms.assetid: 30ff9cf7-bf93-4979-bacd-d76e5dadbef6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 854841685bab015fc0b9a4bc985762df46a7f0c89eae3d38b4b63e081107b70b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119015413"
---
# <a name="auditing"></a>Auditoría

La plataforma Windows filtrado de datos (WFP) proporciona auditoría de eventos relacionados con el firewall y IPsec. Estos eventos se almacenan en el registro de seguridad del sistema.

Los eventos auditados son los siguientes.



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th>Categoría auditoría</th>
<th>Subcategoría de auditoría</th>
<th>Eventos auditados</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Cambio de directiva<br/> {6997984D-797A-11D9-BED3-505054503030}<br/></td>
<td>Filtrado del cambio de directiva de plataforma<br/> {0CCE9233-69AE-11D9-BED3-505054503030}<br/></td>
<td><blockquote>
[!Note]<br />
Los números representan los valores de Event ID como se muestra en Visor de eventos (eventvwr.exe).
</blockquote>
<br/> Adición y eliminación de objetos WFP:<br/>
<ul>
<li>5440 Llamada persistente agregada</li>
<li>5441 Tiempo de arranque o filtro persistente agregado</li>
<li>Se ha agregado el proveedor persistente 5442.</li>
<li>5443 Contexto de proveedor persistente agregado</li>
<li>5444 Subcapa persistente agregada</li>
<li>5446 Llamada en tiempo de ejecución agregada o eliminada</li>
<li>5447 Filtro en tiempo de ejecución agregado o quitado</li>
<li>5448 Proveedor en tiempo de ejecución agregado o quitado</li>
<li>5449 Contexto de proveedor en tiempo de ejecución agregado o quitado</li>
<li>5450 Subcapa en tiempo de ejecución agregada o quitada</li>
</ul></td>
</tr>
<tr class="even">
<td>Acceso a objetos<br/> {6997984A-797A-11D9-BED3-505054503030}<br/></td>
<td>Filtrado de la colocación de paquetes de plataforma <br/> {0CCE9225-69AE-11D9-BED3-505054503030}<br/></td>
<td>Paquetes descartados por WFP:<br/>
<ul>
<li>5152 Paquete eliminado</li>
<li>5153 Paquete veto</li>
</ul></td>
</tr>
<tr class="odd">
<td>Acceso a objetos<br/></td>
<td>Filtrado de la conexión de plataforma <br/> {0CCE9226-69AE-11D9-BED3-505054503030}<br/></td>
<td>Conexiones permitidas y bloqueadas:<br/>
<ul>
<li>5154 Escucha permitida</li>
<li>5155 Escucha bloqueada</li>
<li>5156 Conexión permitida</li>
<li>5157 Conexión bloqueada</li>
<li>5158 Enlace permitido</li>
<li>5159 Enlace bloqueado</li>
</ul>
<blockquote>
[!Note]<br />
Las conexiones permitidas no siempre auditan el identificador del filtro asociado. FilterID para TCP será 0 a menos que se utilice un subconjunto de estas condiciones de filtrado: UserID, AppID, Protocol y Remote Port.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td>Acceso a objetos<br/></td>
<td>Otros eventos de acceso a objetos<br/> {0CCE9227-69AE-11D9-BED3-505054503030}<br/></td>
<td><blockquote>
[!Note]<br />
Esta subcategoría permite muchas auditorías. A continuación se enumeran las auditorías específicas de WFP.
</blockquote>
<br/> Estado de prevención de denegación de servicio:<br/>
<ul>
<li>5148 Se inició el modo de prevención de doS de WFP</li>
<li>5149 Modo de prevención de doS de WFP detenido</li>
</ul></td>
</tr>
<tr class="odd">
<td>Inicio/cierre de sesión<br/> {69979849-797A-11D9-BED3-505054503030}<br/></td>
<td>Modo principal de IPsec<br/> {0CCE9218-69AE-11D9-BED3-505054503030}<br/></td>
<td>Negociación del modo principal de IKE y AuthIP:<br/>
<ul>
<li>4650, 4651 Asociación de seguridad establecida</li>
<li>4652, 4653 Error de negociación</li>
<li>4655 La asociación de seguridad finalizó</li>
</ul></td>
</tr>
<tr class="even">
<td>Inicio/cierre de sesión<br/></td>
<td>Modo rápido de IPsec <br/> {0CCE9219-69AE-11D9-BED3-505054503030}<br/></td>
<td>Negociación del modo rápido de IKE y AuthIP:<br/>
<ul>
<li>5451 Asociación de seguridad establecida</li>
<li>5452 La asociación de seguridad finalizó</li>
<li>4654 Error de negociación</li>
</ul></td>
</tr>
<tr class="odd">
<td>Inicio/cierre de sesión <br/></td>
<td>Modo extendido de IPsec<br/> {0CCE921A-69AE-11D9-BED3-505054503030}<br/></td>
<td>Negociación del modo extendido de AuthIP:<br/>
<ul>
<li>4978 Paquete de negociación no válido</li>
<li>4979, 4980, 4981, 4982 Asociación de seguridad establecida</li>
<li>Error de negociación 4983, 4984</li>
</ul></td>
</tr>
<tr class="even">
<td>Sistema<br/> {69979848-797A-11D9-BED3-505054503030}<br/></td>
<td>Controlador IPsec<br/> {0CCE9213-69AE-11D9-BED3-505054503030}<br/></td>
<td>Paquetes descartados por el controlador IPsec:<br/>
<ul>
<li>4963 Paquete de texto no enviado entrante eliminado</li>
</ul></td>
</tr>
</tbody>
</table>



 

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

