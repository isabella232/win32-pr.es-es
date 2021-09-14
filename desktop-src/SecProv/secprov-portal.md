---
description: Los proveedores WMI de seguridad se pueden usar para el scripting wmi y para crear un proveedor de seguridad administrado.
ms.assetid: c3f7bd91-6cea-43ee-b8a7-1506dbd7926d
title: Proveedores WMI de seguridad
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7d81833abff5160847678d094694702e4711de90
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127068964"
---
# <a name="security-wmi-providers"></a>Proveedores WMI de seguridad

## <a name="purpose"></a>Propósito

Los proveedores WMI de seguridad permiten a los administradores y programadores configurar Cifrado de unidad BitLocker (BDE) y el Módulo de plataforma segura (TPM) mediante Windows Management Instrumentation (WMI).

## <a name="developer-audience"></a>Audiencia de desarrolladores

En este documento se especifica la interfaz del proveedor WMI para administrar y configurar Cifrado de unidad BitLocker (BDE) y Módulo de plataforma segura (TPM) en Windows Server 2008 R2 y Windows Server 2008 para servidores, y Windows 7 y Windows Vista para equipos cliente. Está pensado para que lo lean los que escriben scripts, elementos de la interfaz de usuario u otras herramientas administrativas para BDE o TPM.

## <a name="run-time-requirements"></a>Requisitos de tiempo de ejecución

Los proveedores WMI de seguridad requieren el archivo .mof especificado con cada proveedor y un sistema operativo compatible. El sistema operativo mínimo es Windows Server 2008 o Windows Vista. Cifrado de unidad BitLocker solo está disponible para las versiones Windows Vista Enterprise y Windows Vista Ultimate de Windows Vista. Para obtener información sobre los requisitos en tiempo de ejecución para un elemento de programación determinado, vea la sección Requisitos de la página de referencia de ese elemento.

## <a name="in-this-section"></a>En esta sección



| Tema                                                                               | Descripción                                                        |
|-------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| [Acerca de los proveedores WMI de seguridad](about-security-wmi-providers.md)<br/>         | Breve introducción a los proveedores WMI de seguridad.<br/>           |
| [Referencia de proveedores WMI de seguridad](security-wmi-providers-reference.md)<br/> | Documentación de referencia de los proveedores WMI de seguridad.<br/> |



 

## <a name="additional-resources"></a>Recursos adicionales

Los siguientes son recursos adicionales.



| Recurso     | Descripción                                                                                                                                               |
|--------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| Clases      | Para obtener más información sobre los proveedores WMI de seguridad, [**vea Win32 \_ EncryptableVolume**](win32-encryptablevolume.md) y [**Win32 \_ Tpm**](win32-tpm.md). |



 

 

 




