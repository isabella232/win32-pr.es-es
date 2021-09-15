---
title: Transferencias de datos descargados
description: Transferencias de datos descargados
ms.assetid: 91EBE6D6-2DA7-48DA-AEB7-3FAFCA8341F5
keywords:
- Odx
- copy offload
- Descarga
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1057ed27347fefc7ebc6a171eb7273da4341b024
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127570364"
---
# <a name="offloaded-data-transfers"></a>Transferencias de datos descargados

## <a name="platforms"></a>Plataformas

**Clientes:** Windows 8  
**Servidores:** Windows Server 2012  


## <a name="description"></a>Descripción

Para avanzar en el movimiento de datos de almacenamiento, Microsoft ha desarrollado una nueva tecnología de transferencia de datos: transferencia de datos descargados (ODX). En lugar de usar operaciones de lectura y escritura en búfer en búfer, Windows ODX inicia la operación de copia con una lectura de descarga y recupera un token que representa los datos del dispositivo de almacenamiento y, a continuación, usa un comando de descarga de escritura con el token para solicitar el movimiento de datos desde el disco de origen al disco de destino. El administrador de copia de los dispositivos de almacenamiento realiza el movimiento de datos según el token. En el Windows 8, el administrador de TI y el administrador de almacenamiento pueden usar la característica ODX de Windows para interactuar con el dispositivo de almacenamiento para mover archivos o datos grandes a través de la red de almacenamiento de alta velocidad. Windows ODX reducirá significativamente el tráfico de red cliente-servidor y el uso del tiempo de CPU durante grandes transferencias de datos, ya que todo el movimiento de datos se encuentra en la red de almacenamiento de back-end. ODX se puede usar en la implementación de máquinas virtuales, la migración masiva de datos y la compatibilidad con dispositivos de almacenamiento en capas, y puede reducir el costo de la implementación de hardware físico a través de las características de almacenamiento de aprovisionamiento fino y ODX.

> [!Note]  
> Esta característica solo funcionará en dispositivos de almacenamiento con implementación de especificación SPC4 y SBC3.

 

## <a name="functional-details"></a>Detalles funcionales

-   La Windows ODX se inserta en el motor de copia del Windows operativo; durante la enumeración de almacenamiento, Windows consultará la funcionalidad ODX del dispositivo de almacenamiento.
-   El dispositivo de almacenamiento de origen de copia y el dispositivo de almacenamiento de destino de copia deben administrarse en el mismo administrador de copia para admitir la descarga de copia.
-   Si se produce un error en una operación de descarga de copia, el administrador de copias del dispositivo de almacenamiento debe devolver los datos de sentido adicionales adecuados para el control de errores de las aplicaciones.
-   El motor Windows copia de copia de copia se retendrán en la operación de copia tradicional si se produce un error en la operación de descarga de copia.

## <a name="using-odx"></a>Uso de ODX

-   La aplicación de transferencia de datos debe asegurarse de que tanto el LUN de origen de copia como el LUN de destino de copia son compatibles con ODX antes de llamar a las rutinas de la API de ODX.
-   En Windows, los usuarios podrían usar "arrastrar" o "copiar y pegar" para realizar la descarga de copia.
-   Cuando el LUN de origen y el LUN de destino se montan con el sistema de archivos, la aplicación solo debe llamar a FSCTL Offload Read y FSCTL Offload Write para realizar la transferencia de datos desde el LUN de origen al LUN de \_ \_ \_ \_ destino.
-   Si se produce un error en una operación de descarga de copia, el administrador de copias del dispositivo de almacenamiento debe devolver los datos de sentido adicionales adecuados para el control de errores de las aplicaciones.
-   Cuando el LUN de origen o el LUN de destino no se montan con el sistema de archivos y se bloquean, la aplicación debe llamar a IOCTL STORAGE MANAGE DATA SET ATTRIBUTES con la acción \_ \_ \_ \_ \_ DeviceDsmAction \_ OffloadRead o DeviceDsmAction \_ OffloadWrite para realizar la descarga de copia.
-   Storage aplicaciones de administración pueden usar la API SCSI PASS THROUGH para realizar transferencias de datos descargados cuando los LUN de origen y destino no se montan con ningún sistema de archivos y se \_ \_ bloquean

## <a name="tests"></a>Pruebas

-   Para garantizar una experiencia de usuario sólida, compruebe la Windows ODX de la matriz de almacenamiento.
-   El dispositivo de almacenamiento debe cumplir Windows requisitos de certificación de transferencias de datos descargados (que se usan como logotipo) para admitir la característica ODX.
-   Use el kit Windows de certificación de hardware de transferencias de datos descargados para comprobar la compatibilidad de la característica ODX de los dispositivos de almacenamiento.

## <a name="resources"></a>Recursos

-   T10 XCOPY Lite Spec (11-059r8)
    -   [https://www.t10.org/cgi-bin/ac.pl?t=f&f=spc4r35b.pdf](https://www.t10.org/cgi-bin/ac.pl?t=f&f=spc4r35b.pdf)
    -   [https://www.t10.org/cgi-bin/ac.pl?t=f&f=sbc3r30.pdf](https://www.t10.org/cgi-bin/ac.pl?t=f&f=sbc3r30.pdf)
-   [Servicios de panel de hardware](/windows-hardware/drivers/dashboard/)
-   [Estructura SCSI \_ PASS \_ THROUGH](/windows-hardware/drivers/ddi/ntddscsi/ns-ntddscsi-_scsi_pass_through)

 

 