---
title: Glosario de acceso a dispositivos
description: Estos son los términos que se usan en toda la documentación de la API de acceso a dispositivos.
Robots: noindex, nofollow
ms.assetid: A6311538-D7CC-4A23-A145-14AF3BBFC4C4
ms.topic: article
ms.date: 02/11/2020
ms.openlocfilehash: 8406c41a2666f9014bac27452572c6f88b84e6bf
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127570948"
---
# <a name="device-access-glossary"></a>Glosario de acceso a dispositivos

Estos son los términos que se usan en toda la documentación de la API de acceso a dispositivos.

<dl> <dt>

**AppContainer**
</dt> <dd>

Entorno de ejecución muy restringido en el que se ejecuta un proceso con un subconjunto reducido de privilegios del usuario. Un proceso que se ejecuta dentro de un AppContainer se denomina proceso AppContainer. Un proceso AppContainer está aislado de otros procesos de AppContainer y del perfil del usuario. Tiene acceso limitado a un subconjunto muy pequeño de recursos del sistema, como archivos, dispositivos, claves del Registro, puntos de conexión de comunicación entre procesos (IPC)/llamada a procedimiento remoto (RPC) y recursos de red.

</dd> <dt>

**Binding**
</dt> <dd>

Asociar un objeto de acceso de dispositivo a una interfaz de dispositivo determinada. Si el enlace se realiza correctamente, Windows store puede usar el objeto de acceso del dispositivo como agente para comunicarse con el controlador de dispositivo.

</dd> <dt>

**Agente**
</dt> <dd>

Componente que proporciona acceso a un recurso que no se concede de forma predeterminada.

</dd> <dt>

**Aplicación con privilegios**
</dt> <dd>

Una aplicación que se identifica en los metadatos de un dispositivo determinado como asociada a ese dispositivo, para que pueda comunicarse con la interfaz restringida del controlador del dispositivo. Un ejemplo de este tipo de aplicación podría ser una aplicación de reproducción de música propietaria que tiene permiso exclusivo para sincronizarse con un reproductor de música portátil, cuando las aplicaciones de la competencia no pueden. Para obtener más información sobre cómo establecer los metadatos de un dispositivo o cómo restringir un controlador a aplicaciones con privilegios, consulta Aplicaciones de dispositivo [UWP para dispositivos internos.](/windows-hardware/drivers/devapps/uwp-device-apps-for-specialized-devices)

</dd> </dl>
