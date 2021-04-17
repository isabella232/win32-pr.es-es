---
description: Un registro de grupo son datos específicos que se publican en todos los miembros activos de un grupo del mismo nivel, por ejemplo, un mensaje de chat o una actualización de estado específica de la aplicación.
ms.assetid: 073ee4e9-0e97-451a-a808-8265575d073c
title: Administrar registros de grupo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3b6d9e3257cc597b715dc9c65eb5945c00c15286
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105667416"
---
# <a name="managing-group-records"></a>Administrar registros de grupo

Un registro de grupo son datos específicos que se publican en todos los miembros activos de un grupo del mismo nivel, por ejemplo, un mensaje de chat o una actualización de estado específica de la aplicación. Un registro se representa mediante la estructura del [**\_ registro del mismo nivel**](/windows/desktop/api/P2P/ns-p2p-peer_record) y contiene la siguiente información sobre un elemento del mismo nivel:

-   El ID. de registro es un valor que identifica de forma única un registro en el grupo del mismo nivel.
-   GUID que especifica el tipo de registro. Las aplicaciones pueden admitir distintos tipos de registros. Una aplicación interpreta el campo de **datos** de un registro basándose en el tipo de registro. Algunos GUID están reservados y la llamada a la API devuelve **peer \_ e \_ no \_ autorizado** cuando la aplicación intenta utilizarlos.
-   Conjunto de atributos de registro que se describe como una cadena XML. Los atributos se usan al buscar registros. Para obtener más información sobre los atributos, consulte [registro del esquema de atributo](record-attribute-schema.md).
-   La hora del mismo nivel en la que se crea un registro.
-   El tiempo del mismo nivel que expira un registro.
-   La hora del mismo nivel en la que se modifica un registro.
-   Creador de un registro.
-   Miembro que modifica un registro.
-   Una estructura de [**\_ datos del mismo nivel**](/windows/desktop/api/P2P/ns-p2p-peer_data) que contiene la firma criptográfica para todos los campos de esta estructura de [**\_ registro del mismo nivel**](/windows/desktop/api/P2P/ns-p2p-peer_record) . Este campo no se puede actualizar ni modificar directamente en un elemento del mismo nivel.
-   Una estructura de [**\_ datos del mismo nivel**](/windows/desktop/api/P2P/ns-p2p-peer_data) que contiene los datos específicos de la aplicación asociados a este registro como una matriz de bytes. El tipo de datos presente en este campo viene determinado por el tipo de registro definido por la aplicación.

## <a name="obtaining-peer-group-records"></a>Obtención de registros de grupo del mismo nivel

Los registros individuales se obtienen mediante una llamada a [**PeerGroupGetRecord**](/windows/desktop/api/P2P/nf-p2p-peergroupgetrecord) con el identificador del registro. Al procesar todos los registros de un tipo específico, el conjunto enumerado de todos los registros de grupo del mismo nivel actuales se obtiene mediante una llamada a [**PeerGroupEnumRecords**](/windows/desktop/api/P2P/nf-p2p-peergroupenumrecords) para abrir la enumeración y, a continuación, llamar a [**PeerGetNextItem**](/windows/desktop/api/P2P/nf-p2p-peergetnextitem) de forma iterativa hasta que se recuperen todos los registros. Cuando termine, cierre la enumeración y libere la memoria asociada a ella mediante una llamada a [**PeerEndEnumeration**](/windows/desktop/api/P2P/nf-p2p-peerendenumeration).

Cuando un elemento del mismo nivel crea, elimina o actualiza un registro, el registro afectado se publica en todos los miembros del grupo del mismo nivel mediante el evento de **cambio de registro de eventos de grupo del mismo nivel \_ \_ \_ \_** . Tenga en cuenta que si un elemento del mismo nivel no está conectado al grupo, recibirá el registro actualizado la próxima vez que se conecte. Es importante registrarse para este evento con [**PeerGroupRegisterEvent**](/windows/desktop/api/P2P/nf-p2p-peergroupregisterevent) si la aplicación mantiene o administra registros de una manera significativa. Como alternativa, la aplicación puede consultar la base de datos de registros a petición mediante [**PeerGroupSearchRecords**](/windows/desktop/api/P2P/nf-p2p-peergroupsearchrecords).

Cuando se genera el evento de **cambio de registro de eventos de grupo del mismo nivel \_ \_ \_ \_** , el identificador de registro y el tipo específicos, así como el tipo de cambio (agregar, actualizar, eliminar) se reciben como una estructura de [**datos de cambio de \_ registro de eventos \_ \_ \_ del mismo nivel**](/windows/desktop/api/P2P/ns-p2p-peer_event_record_change_data) . Esta estructura se obtiene con una llamada a [**PeerGroupGetEventData**](/windows/desktop/api/P2P/nf-p2p-peergroupgeteventdata). Si el cambio es una adición o una actualización, debe usar [**PeerGroupGetRecord**](/windows/desktop/api/P2P/nf-p2p-peergroupgetrecord) para obtener el registro con el identificador proporcionado. La base de datos de registros local de la infraestructura de se actualiza automáticamente.

También puede buscar registros específicos en función de los atributos personalizados específicos proporcionados en el campo **pwzAttributes** del [**\_ registro del mismo nivel**](/windows/desktop/api/P2P/ns-p2p-peer_record), así como los atributos predefinidos. Para ello, utilice la función [**PeerGroupSearchRecords**](/windows/desktop/api/P2P/nf-p2p-peergroupsearchrecords) con una consulta de búsqueda XML con el formato especificado en el tema [formato de consulta de búsqueda de registros](record-search-query-format.md) .

Para obtener más información sobre cómo trabajar con registros en la infraestructura del mismo nivel, consulte el tema [registros](records.md) en [uso de la infraestructura del mismo nivel](using-the-peer-infrastructure.md).

## <a name="administration-of-peer-group-records"></a>Administración de registros de grupo del mismo nivel

Cuando el creador del grupo del mismo nivel emite las invitaciones iniciales, puede especificar que determinados miembros actúen en un rol administrativo (Administrador del rol de grupo del mismo nivel \_ \_ \_ ) cada vez que emita nuevas credenciales al usuario (a través de [**PeerGroupCreateInvitation**](/windows/desktop/api/P2P/nf-p2p-peergroupcreateinvitation) o [**PeerGroupIssueCredentials**](/windows/desktop/api/P2P/nf-p2p-peergroupissuecredentials)). Un administrador tiene la capacidad de agregar, eliminar y actualizar directamente cualquier registro de grupo del mismo nivel. Por el contrario, un miembro del grupo del mismo nivel con su rol establecido **en \_ \_ \_ miembro del rol de grupo del mismo nivel** o en el rol de **Grupo del mismo nivel que invita a un \_ \_ \_ \_ miembro** solo puede Agregar, actualizar y eliminar sus propios registros.

El creador tiene el rol de administrador de forma predeterminada.

Para actualizar un registro, obtenga el registro con [**PeerGroupGetRecord**](/windows/desktop/api/P2P/nf-p2p-peergroupgetrecord) o [**PeerGroupEnumRecords**](/windows/desktop/api/P2P/nf-p2p-peergroupenumrecords), realice los cambios y pase el registro actualizado a [**PeerGroupUpdateRecord**](/windows/desktop/api/P2P/nf-p2p-peergroupupdaterecord).

Para eliminar un registro, pase el identificador de registro que se va a eliminar a [**PeerGroupDeleteRecord**](/windows/desktop/api/P2P/nf-p2p-peergroupdeleterecord).

Para agregar un registro, cree una nueva estructura de [**\_ registro del mismo nivel**](/windows/desktop/api/P2P/ns-p2p-peer_record) y rellene los campos siguientes:

-   **dwSize**. Este campo contiene el valor de **sizeof**([**\_ registro del mismo nivel**](/windows/desktop/api/P2P/ns-p2p-peer_record)).
-   **ftExpiration**. Este campo contiene la fecha y hora de expiración de este registro, expresadas en el momento del mismo nivel como una estructura **FILETIME** .
-   **Escriba**. Este campo contiene un valor **GUID** que identifica el tipo de registro para la aplicación. Si este tipo es personalizado para la infraestructura de la aplicación, también debe rellenar el campo de **datos** .

Los campos siguientes se rellenan mediante la infraestructura de y se omitirán si la aplicación la establece:

-   **id**
-   **pwzCreatorId**
-   **pwzLastModifiedById**
-   **ftCreation**
-   **ftLastModified**
-   **securityData**

Los campos restantes son opcionales. Para agregar este nuevo registro al grupo del mismo nivel, páselo a [**PeerGroupAddRecord**](/windows/desktop/api/P2P/nf-p2p-peergroupaddrecord).

## <a name="importing-and-exporting-records"></a>Importar y exportar registros

Los registros de grupo punto a punto se mantienen localmente como una base de datos. Para guardar una instantánea actual de la base de datos de registros de grupo del mismo nivel en un archivo local, llame a [**PeerGroupExportDatabase**](/windows/desktop/api/P2P/nf-p2p-peergroupexportdatabase)y pásele el identificador al grupo del mismo nivel. A continuación, este archivo se puede transportar a otro equipo o aplicación, que puede extraer y usar esta base de datos de registros llamando a [**PeerGroupImportDatabase**](/windows/desktop/api/P2P/nf-p2p-peergroupimportdatabase).

 

 



