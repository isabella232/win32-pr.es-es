---
title: Auditoría
description: La plataforma de filtrado de Windows (WFP) proporciona auditoría de eventos relacionados con IPsec y firewall.
ms.assetid: 30ff9cf7-bf93-4979-bacd-d76e5dadbef6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3cef1d4fee81afc366a987575935c1de8880092c
ms.sourcegitcommit: db89157e3be911fdce2e543e99faa31fb2403bc8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/18/2020
ms.locfileid: "103995797"
---
# <a name="auditing"></a>Auditoría

La plataforma de filtrado de Windows (WFP) proporciona auditoría de eventos relacionados con IPsec y firewall. Estos eventos se almacenan en el registro de seguridad del sistema.

Los eventos auditados son los siguientes.



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th>Categoría de auditoría</th>
<th>Subcategoría de auditoría</th>
<th>Eventos auditados</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Cambio de directiva<br/> {6997984D-797A-11D9-BED3-505054503030}<br/></td>
<td>Filtrar cambio de directiva de plataforma<br/> {0CCE9233-69AE-11D9-BED3-505054503030}<br/></td>
<td><blockquote>
[!Note]<br />
Los números representan los identificadores de evento que se muestran en Visor de eventos (eventvwr.exe).
</blockquote>
<br/> Adición y eliminación de objetos de WFP:<br/>
<ul>
<li>5440 llamada persistente agregada</li>
<li>5441 tiempo de arranque o filtro persistente agregado</li>
<li>5442 proveedor persistente agregado</li>
<li>5443 contexto de proveedor persistente agregado</li>
<li>5444 subcapa persistente agregada</li>
<li>llamada en tiempo de ejecución de 5446 agregada o quitada</li>
<li>5447 filtro en tiempo de ejecución agregado o quitado</li>
<li>5448 proveedor en tiempo de ejecución agregado o quitado</li>
<li>5449 contexto de proveedor en tiempo de ejecución agregado o quitado</li>
<li>5450 subcapa en tiempo de ejecución agregada o quitada</li>
</ul></td>
</tr>
<tr class="even">
<td>Acceso a objetos<br/> {6997984A-797A-11D9-BED3-505054503030}<br/></td>
<td>Filtrar eliminación de paquetes de plataforma <br/> {0CCE9225-69AE-11D9-BED3-505054503030}<br/></td>
<td>Paquetes descartados por WFP:<br/>
<ul>
<li>paquete 5152 quitado</li>
<li>paquete 5153 vetado</li>
</ul></td>
</tr>
<tr class="odd">
<td>Acceso a objetos<br/></td>
<td>Filtrar conexión de plataforma <br/> {0CCE9226-69AE-11D9-BED3-505054503030}<br/></td>
<td>Conexiones permitidas y bloqueadas:<br/>
<ul>
<li>5154 escucha permitida</li>
<li>5155 escucha bloqueada</li>
<li>5156 conexión permitida</li>
<li>5157 conexión bloqueada</li>
<li>5158 enlace permitido</li>
<li>5159 enlace bloqueado</li>
</ul>
<blockquote>
[!Note]<br />
Las conexiones permitidas no siempre auditan el identificador del filtro asociado. El valor de FilterID para TCP será 0 a menos que se use un subconjunto de estas condiciones de filtrado: UserID, AppID, protocolo, Puerto remoto.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td>Acceso a objetos<br/></td>
<td>Otros eventos de acceso a objetos<br/> {0CCE9227-69AE-11D9-BED3-505054503030}<br/></td>
<td><blockquote>
[!Note]<br />
Esta subcategoría habilita muchas auditorías. A continuación se enumeran las auditorías específicas de WFP.
</blockquote>
<br/> Estado de prevención de denegación de servicio:<br/>
<ul>
<li>5148 modo de prevención de DoS de WFP iniciado</li>
<li>5149 modo de prevención de DoS de WFP detenido</li>
</ul></td>
</tr>
<tr class="odd">
<td>Inicio/cierre de sesión<br/> {69979849-797A-11D9-BED3-505054503030}<br/></td>
<td>Modo principal de IPsec<br/> {0CCE9218-69AE-11D9-BED3-505054503030}<br/></td>
<td>Negociación del modo principal de IKE y AuthIP:<br/>
<ul>
<li>4650, 4651 Asociación de seguridad establecida</li>
<li>4652, error de negociación de 4653</li>
<li>4655 finalizó la Asociación de seguridad</li>
</ul></td>
</tr>
<tr class="even">
<td>Inicio/cierre de sesión<br/></td>
<td>Modo rápido de IPsec <br/> {0CCE9219-69AE-11D9-BED3-505054503030}<br/></td>
<td>Negociación de modo rápido de IKE y AuthIP:<br/>
<ul>
<li>5451 Asociación de seguridad establecida</li>
<li>5452 finalizó la Asociación de seguridad</li>
<li>error de negociación 4654</li>
</ul></td>
</tr>
<tr class="odd">
<td>Inicio/cierre de sesión <br/></td>
<td>Modo extendido de IPsec<br/> {0CCE921A-69AE-11D9-BED3-505054503030}<br/></td>
<td>Negociación del modo extendido de AuthIP:<br/>
<ul>
<li>4978 paquete de negociación no válido</li>
<li>4979, 4980, 4981, 4982 Asociación de seguridad establecida</li>
<li>4983, error de negociación de 4984</li>
</ul></td>
</tr>
<tr class="even">
<td>System<br/> {69979848-797A-11D9-BED3-505054503030}<br/></td>
<td>Controlador IPsec<br/> {0CCE9213-69AE-11D9-BED3-505054503030}<br/></td>
<td>Paquetes descartados por el controlador IPsec:<br/>
<ul>
<li>4963 paquete de texto no cifrado entrante quitado</li>
</ul></td>
</tr>
</tbody>
</table>



 

De forma predeterminada, la auditoría de WFP está deshabilitada.

La auditoría se puede habilitar por categoría a través del complemento MMC de Editor de objetos de directiva de grupo, el complemento MMC Directiva de seguridad local o el comando auditpol.exe.

Por ejemplo, para habilitar la auditoría de eventos de cambio de Directiva, puede:

-   Usar el Editor de objetos de directiva de grupo

    1.  Ejecute **gpedit. msc**.
    2.  Expanda Directiva de equipo local.
    3.  Expanda configuración del equipo.
    4.  Expanda configuración de Windows.
    5.  Expanda configuración de seguridad.
    6.  Expanda directivas locales.
    7.  Haz clic en Directiva de auditoría.
    8.  Haga doble clic en auditar cambio de directiva para iniciar el cuadro de diálogo Propiedades.
    9.  Active las casillas aciertos y errores.

-   Usar la Directiva de seguridad local

    1.  Ejecute **SECPOL. msc**.
    2.  Expanda directivas locales.
    3.  Haz clic en Directiva de auditoría.
    4.  Haga doble clic en auditar cambio de directiva para iniciar el cuadro de diálogo Propiedades.
    5.  Active las casillas aciertos y errores.

-   Usar el comando auditpol.exe

    -   **AuditPol/Set/Category: "cambio de directiva"/Success: enable/Failure: enable**

La auditoría se puede habilitar en cada subcategoría solo a través del comando auditpol.exe.

La categoría de auditoría y los nombres de subcategoría están localizados. Para evitar la localización de scripts de auditoría, se pueden usar los GUID correspondientes en lugar de los nombres.

Por ejemplo, para habilitar la auditoría de eventos de cambio de directiva de plataforma de filtrado, puede usar uno de los siguientes comandos:

-   **AuditPol/Set/subcategory: "filtrar cambio de directiva de plataforma"/Success: enable/Failure: enable**
-   **AuditPol/Set/subcategory: "{0CCE9233-69AE-11D9-BED3-505054503030}"/Success: enable/Failure: enable**

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[AuditPol](/previous-versions/windows/it-pro/windows-server-2012-R2-and-2012/cc731451(v=ws.11))
</dt> <dt>

[Registro de eventos](/previous-versions/orphan-topics/ws.10/dd996684(v=ws.10))
</dt> <dt>

[Directiva de grupo](/windows/deployment/deploy-whats-new)
</dt> </dl>

