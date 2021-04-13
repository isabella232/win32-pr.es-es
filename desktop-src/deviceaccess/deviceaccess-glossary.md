---
title: Glosario de acceso a dispositivos
description: A continuación se indican los términos que se usan en la documentación de la API de acceso a dispositivos.
Robots: noindex, nofollow
ms.assetid: A6311538-D7CC-4A23-A145-14AF3BBFC4C4
ms.topic: article
ms.date: 02/11/2020
ms.openlocfilehash: 8406c41a2666f9014bac27452572c6f88b84e6bf
ms.sourcegitcommit: 01a4383738056cf3de4f45f36d98ef73d4dc694d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/11/2020
ms.locfileid: "104420213"
---
# <a name="device-access-glossary"></a>Glosario de acceso a dispositivos

A continuación se indican los términos que se usan en la documentación de la API de acceso a dispositivos.

<dl> <dt>

**AppContainer**
</dt> <dd>

Entorno de ejecución muy restringido en el que se ejecuta un proceso con un subconjunto reducido de privilegios del usuario. Un proceso que se ejecuta dentro de un AppContainer se denomina proceso AppContainer. Un proceso de AppContainer está aislado de otros procesos de AppContainer y del perfil del usuario. Tiene acceso limitado a un subconjunto muy pequeño de recursos del sistema, como archivos, dispositivos, claves del registro, puntos de conexión de la llamada a procedimiento de la comunicación entre procesos (IPC)/Remote y recursos de red.

</dd> <dt>

**Binding**
</dt> <dd>

Asociar un objeto de acceso de dispositivo a una interfaz de dispositivo determinada. Si el enlace se realiza correctamente, las aplicaciones de la tienda Windows pueden usar el objeto de acceso de dispositivo como agente para comunicarse con el controlador de dispositivo.

</dd> <dt>

**Agente**
</dt> <dd>

Componente que proporciona acceso a un recurso que no se concede de forma predeterminada.

</dd> <dt>

**Aplicación con privilegios**
</dt> <dd>

Una aplicación que se identifica en los metadatos de un dispositivo determinado como asociado a ese dispositivo, de modo que pueda comunicarse con la interfaz restringida del controlador de dispositivo. Un ejemplo de este tipo de aplicación podría ser una aplicación de reproducción de música de su propiedad que tiene permiso exclusivo para la sincronización con un reproductor de música portátil, cuando las aplicaciones de la competencia no pueden. Para obtener más información sobre cómo establecer los metadatos de un dispositivo o cómo restringir un controlador a las aplicaciones con privilegios, consulte [aplicaciones de dispositivo UWP para dispositivos internos](/windows-hardware/drivers/devapps/uwp-device-apps-for-specialized-devices).

</dd> </dl>
