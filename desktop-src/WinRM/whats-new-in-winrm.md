---
title: Novedades de WinRM 2.0
description: Las nuevas características están disponibles en Windows administración remota versión 2.0. (WinRM 2.0).
ms.assetid: 402c179a-6dd7-4d75-9318-bb8194b5527d
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: d322b0b86600cd783bd787427b53df334f3d499a
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2021
ms.locfileid: "122480591"
---
# <a name="whats-new-in-winrm-20"></a>Novedades de WinRM 2.0

Las nuevas características están disponibles en Windows administración remota versión 2.0. (WinRM 2.0)

WinRM 2.0 se incluye en Windows Server 2008 R2 y Windows 7.

También puede descargar WinRM 2.0 para Windows Server 2008 con Service Pack 2 (SP2) y Windows Vista con Service Pack 2 (SP2). Para obtener información sobre cómo descargar WinRM 2.0, vea [KB968929](https://support.microsoft.com/kb/968929).

En la tabla siguiente se muestra la documentación de WinRM 2.0.




| Tema | Descripción | 
|-------|-------------|
| <a href="client-shell-api.md">API de Shell de cliente de WinRM</a><br /> | La interfaz de programación de aplicaciones (API) de WinRM Client Shell proporciona funcionalidad para crear y administrar shells y operaciones de shell, comandos y flujos de datos en equipos remotos. <br /> | 
| <a href="winrm-plugin-api.md">API del complemento WinRM</a><br /> | WinRM Plug-in API proporciona funcionalidad que permite a un usuario escribir complementos mediante la implementación de determinadas API para las operaciones y los URI de <a href="windows-remote-management-glossary.md"><em>recursos</em></a> admitidos.<br /> | 
| <a href="winrm-application-hosting.md">Infraestructura para administrar servicios hospedados</a><br /> | WinRM 2.0 presenta un marco de hospedaje. Se admiten dos modelos de hospedaje. Una está basada en Internet Information Service (IIS) y la otra está basada en el servicio WinRM. <br /> Para obtener más información sobre la configuración del host, vea los temas siguientes:<br /><ul><li><a href="iis-host-plug-in-configuration.md">Configuración del complemento de host de IIS</a></li><li><a href="wsman-service-plug-in-configuration.md">Configuración del complemento del servicio WinRM</a></li></ul> | 
| <a href="dmtf-association-traversal.md">Detección de perfiles DMTF mediante el recorrido de asociación</a><br /> | El recorrido de asociación permite a un usuario recuperar instancias de clases association mediante un mecanismo de filtrado estándar.<br /> | 
| <a href="remote-shell-infrastructure-improvements.md">Mejoras en la infraestructura de Remote Shell</a><br /> | En este tema se incluye información sobre las mejoras de infraestructura remota para WinRM. <br /> | 
| <a href="multi-hop-support.md">Compatibilidad con varios saltos</a><br /> | Se ha agregado funcionalidad a WinRM 2.0 que admite la delegación de credenciales de usuario en varios equipos remotos. <br /> El <a href="authentication-constants.md"><strong>tema Constantes de autenticación</strong></a> se actualizó para agregar la siguiente constante: <strong>WSManFlagUseCredSsp</strong>.<br /> Se agregó la siguiente API de C++ para proporcionar compatibilidad con varios saltos: <a href="/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsmanex3"><strong>IWSManEx3</strong></a>.<br /> Se agregó la SIGUIENTE API de scripting para proporcionar compatibilidad con varios saltos: <a href="wsman-sessionflagusecredssp.md"><strong>WSMan.SessionFlagUseCredSsp</strong></a>.<br /> | 
| <a href="quotas.md">Administración de cuotas para shells remotos</a><br /> | En este tema se incluye información sobre la configuración de cuota para la administración remota del shell.<br /> | 
| <a href="winrm-powershell-commandlets.md">Referencia administrada para WS-Management comandos de PowerShell</a><br /> | Los usuarios de WinRM 2.0 pueden usar Windows PowerShell cmdlets para la administración del sistema.<br /> | 




 

 

 





