---
description: Las funciones de archivo de red proporcionan una manera de supervisar y cerrar los recursos de archivo, dispositivo y canalización abiertos en un servidor. Las funciones de archivo se enumeran a continuación.
ms.assetid: cbcdad6e-80dd-49f0-9d69-a82a7010f10b
title: Funciones netFile (Administración de recursos compartidos de red)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8efdd1a9339701ccbb534a91b9dfe0423bea546e8d474455c2a6ffdda02adab1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118362616"
---
# <a name="netfile-functions-network-share-management"></a>Funciones netFile (Administración de recursos compartidos de red)

Las funciones de archivo de red proporcionan una manera de supervisar y cerrar los recursos de archivo, dispositivo y canalización abiertos en un servidor. Las funciones de archivo se enumeran a continuación.



| Función                                 | Descripción                                                          |
|------------------------------------------|----------------------------------------------------------------------|
| [**NetFileClose**](/windows/desktop/api/Lmshare/nf-lmshare-netfileclose)     | Fuerza el cierre de un recurso.                                          |
| [**NetFileEnum**](/windows/desktop/api/Lmshare/nf-lmshare-netfileenum)       | Devuelve información sobre los archivos abiertos en un servidor.                    |
| [**NetFileGetInfo**](/windows/desktop/api/Lmshare/nf-lmshare-netfilegetinfo) | Devuelve información sobre una apertura determinada de un recurso de servidor. |



 

Llame a [**la función NetFileClose**](/windows/desktop/api/Lmshare/nf-lmshare-netfileclose) cuando el archivo no se pueda cerrar por ningún otro medio. Esta función debe usarse con precaución porque **NetFileClose** no escribe los datos almacenados en caché en el sistema cliente en el archivo antes de cerrar el archivo.

La [**función NetFileEnum**](/windows/desktop/api/Lmshare/nf-lmshare-netfileenum) devuelve información sobre los recursos abiertos en un servidor. Una o varias aplicaciones pueden abrir un archivo una o varias veces. Cada apertura de archivo se identifica de forma única. La **función NetFileEnum** devuelve una entrada para cada apertura de archivos. La [**función NetFileGetInfo**](/windows/desktop/api/Lmshare/nf-lmshare-netfilegetinfo) devuelve información sobre una apertura de un recurso.

La información de archivo está disponible en los niveles siguientes.

<dl>

[**FILE \_ INFO \_ 2**](/windows/desktop/api/Lmshare/ns-lmshare-file_info_2)  
[**FILE \_ INFO \_ 3**](/windows/desktop/api/Lmshare/ns-lmshare-file_info_3)  
</dl>

No se admiten los niveles 0 y 1. El nivel 2 devuelve solo el número de identificación asignado al recurso cuando se abrió. El nivel 3 devuelve el número de identificación, los permisos, los bloqueos de archivo y el nombre del usuario que abrió el recurso.

Si está programando para Active Directory, es posible que pueda llamar a determinados métodos de la interfaz de servicio (ADSI) de Active Directory para lograr la misma funcionalidad que puede lograr llamando a las funciones [**NetFileEnum**](/windows/desktop/api/Lmshare/nf-lmshare-netfileenum) y [**NetFileGetInfo.**](/windows/desktop/api/Lmshare/nf-lmshare-netfilegetinfo) Para obtener más información, [**vea IADsResource**](/windows/desktop/api/iads/nn-iads-iadsresource) and [**IADsFileServiceOperations**](/windows/desktop/api/iads/nn-iads-iadsfileserviceoperations).

 

 
