---
description: Un registro de grupo son datos específicos publicados para todos los miembros activos de un grupo del mismo nivel, por ejemplo, un mensaje de chat o una actualización de estado específica de la aplicación.
ms.assetid: 073ee4e9-0e97-451a-a808-8265575d073c
title: Administración de registros de grupo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3b6d9e3257cc597b715dc9c65eb5945c00c15286
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127069223"
---
# <a name="managing-group-records"></a>Administración de registros de grupo

Un registro de grupo son datos específicos publicados para todos los miembros activos de un grupo del mismo nivel, por ejemplo, un mensaje de chat o una actualización de estado específica de la aplicación. Un registro se representa mediante la [**estructura PEER \_ RECORD**](/windows/desktop/api/P2P/ns-p2p-peer_record) y contiene la siguiente información sobre un mismo nivel:

-   El identificador de registro es un valor que identifica de forma única un registro en el grupo del mismo nivel.
-   GUID que especifica el tipo de registro. Las aplicaciones pueden admitir diferentes tipos de registros. Una aplicación interpreta el campo **de datos** de un registro en función del tipo de registro. Algunos GUID están reservados y la llamada API devuelve **PEER E NOT AUTHORIZED \_ \_ \_ cuando** la aplicación intenta usarlos.
-   Conjunto de atributos de registro descritos como una cadena XML. Los atributos se usan al buscar registros. Para obtener más información sobre los atributos, vea [Esquema de atributo de registro.](record-attribute-schema.md)
-   Hora del mismo nivel en la que se crea un registro.
-   El tiempo del mismo nivel que expira un registro.
-   Hora del mismo nivel en la que se modifica un registro.
-   Creador de un registro.
-   Miembro que modifica un registro.
-   Estructura [**PEER \_ DATA que**](/windows/desktop/api/P2P/ns-p2p-peer_data) contiene la firma criptográfica para todos los campos de esta estructura PEER [**\_ RECORD.**](/windows/desktop/api/P2P/ns-p2p-peer_record) Un par no puede actualizar ni modificar directamente este campo.
-   Estructura [**PEER \_ DATA**](/windows/desktop/api/P2P/ns-p2p-peer_data) que contiene los datos específicos de la aplicación asociados a este registro como una matriz de bytes. El tipo de datos presente en este campo viene determinado por el tipo de registro definido por la aplicación.

## <a name="obtaining-peer-group-records"></a>Obtención de registros de grupo del mismo nivel

Los registros individuales se obtienen mediante una llamada [**a PeerGroupGetRecord**](/windows/desktop/api/P2P/nf-p2p-peergroupgetrecord) con el identificador del registro. Al procesar todos los registros de un tipo específico, el conjunto enumerado de todos los registros de grupo del mismo nivel actuales se obtiene llamando primero a [**PeerGroupEnumRecords**](/windows/desktop/api/P2P/nf-p2p-peergroupenumrecords) para abrir la enumeración y, a continuación, llamando iterativamente a [**PeerGetNextItem**](/windows/desktop/api/P2P/nf-p2p-peergetnextitem) hasta que se recuperan todos los registros. Cuando termine, cierre la enumeración y libere la memoria asociada a ella mediante una llamada [**a PeerEndEnumeration**](/windows/desktop/api/P2P/nf-p2p-peerendenumeration).

Cuando un elemento del mismo nivel crea, elimina o actualiza un registro, el registro afectado se publica en todos los miembros del grupo del mismo nivel mediante el evento **PEER GROUP EVENT RECORD \_ \_ \_ \_ CHANGE.** Tenga en cuenta que si un par no está conectado al grupo, recibirá el registro actualizado la próxima vez que se conecte. Es importante registrarse para este evento con [**PeerGroupRegisterEvent**](/windows/desktop/api/P2P/nf-p2p-peergroupregisterevent) si la aplicación mantiene o administra registros de cualquier manera significativa. Como alternativa, la aplicación puede consultar la base de datos de registros a petición [**mediante PeerGroupSearchRecords**](/windows/desktop/api/P2P/nf-p2p-peergroupsearchrecords).

Cuando se genera el evento **PEER GROUP EVENT RECORD \_ \_ \_ \_ CHANGE,** el identificador y el tipo de registro específicos, así como el tipo de cambio (agregar, actualizar, eliminar) se reciben como una estructura [**CHANGE \_ \_ \_ \_ DATA**](/windows/desktop/api/P2P/ns-p2p-peer_event_record_change_data) de REGISTRO DE EVENTOS DEL MISMO NIVEL. Esta estructura se obtiene con una llamada a [**PeerGroupGetEventData**](/windows/desktop/api/P2P/nf-p2p-peergroupgeteventdata). Si el cambio es una adición o una actualización, debe usar [**PeerGroupGetRecord**](/windows/desktop/api/P2P/nf-p2p-peergroupgetrecord) para obtener el registro con el identificador proporcionado. La base de datos de registros local para la infraestructura se actualiza automáticamente.

También puede buscar registros específicos basados en atributos **personalizados específicos proporcionados** en el campo pwzAttributes de [**PEER \_ RECORD**](/windows/desktop/api/P2P/ns-p2p-peer_record), así como cualquier atributo predefinido. Para ello, use la función [**PeerGroupSearchRecords**](/windows/desktop/api/P2P/nf-p2p-peergroupsearchrecords) con una consulta de búsqueda XML con el formato especificado en el tema Formato de consulta de búsqueda [de](record-search-query-format.md) registros.

Para obtener más información sobre cómo trabajar con registros en la infraestructura del mismo nivel, consulte el tema [Registros](records.md) en Uso de [la infraestructura del mismo nivel](using-the-peer-infrastructure.md).

## <a name="administration-of-peer-group-records"></a>Administración de registros de grupo del mismo nivel

Cuando el creador del grupo del mismo nivel emite las invitaciones iniciales, puede especificar que determinados miembros atienden en un rol administrativo (ADMINISTRADOR DE ROLES DE GRUPO DEL MISMO NIVEL) siempre que emita nuevas credenciales al usuario (a través de \_ \_ \_ [**PeerGroupCreateInvitation**](/windows/desktop/api/P2P/nf-p2p-peergroupcreateinvitation) o [**PeerGroupIssueCredentials).**](/windows/desktop/api/P2P/nf-p2p-peergroupissuecredentials) Un administrador tiene la capacidad de agregar, eliminar y actualizar directamente cualquier registro de grupo del mismo nivel. Por el contrario, un miembro del grupo del mismo nivel con su rol establecido en MIEMBRO DE ROL DE GRUPO DEL MISMO NIVEL o MIEMBRO INVITADOR DE ROL DE GRUPO DEL MISMO NIVEL solo puede agregar, actualizar y eliminar sus propios registros. **\_ \_ \_ \_** **\_ \_ \_**

El creador tiene el rol de administrador de forma predeterminada.

Para actualizar un registro, obtenga el registro [**con PeerGroupGetRecord**](/windows/desktop/api/P2P/nf-p2p-peergroupgetrecord) o [**PeerGroupEnumRecords,**](/windows/desktop/api/P2P/nf-p2p-peergroupenumrecords)realice los cambios y pase el registro actualizado a [**PeerGroupUpdateRecord.**](/windows/desktop/api/P2P/nf-p2p-peergroupupdaterecord)

Para eliminar un registro, pase el identificador de registro que se eliminará a [**PeerGroupDeleteRecord.**](/windows/desktop/api/P2P/nf-p2p-peergroupdeleterecord)

Para agregar un registro, cree una nueva estructura [**PEER \_ RECORD**](/windows/desktop/api/P2P/ns-p2p-peer_record) y rellene los campos siguientes:

-   **dwSize**. Este campo contiene el valor de **sizeof**([**PEER \_ RECORD**](/windows/desktop/api/P2P/ns-p2p-peer_record)).
-   **ftExpiration**. Este campo contiene la fecha y hora de expiración de este registro, expresados en tiempo del mismo nivel como **una estructura FILETIME.**
-   **escriba**. Este campo contiene un **valor GUID** que identifica el tipo de registro para la aplicación. Si este tipo es personalizado para la infraestructura de la aplicación, también debe rellenar el campo **de** datos.

La infraestructura rellena los campos siguientes y se omitirán si la aplicación lo establece:

-   **id**
-   **pwzCreatorId**
-   **pwzLastModifiedById**
-   **ftCreation**
-   **ftLastModified**
-   **securityData**

Los campos restantes son opcionales. Para agregar este nuevo registro al grupo del mismo nivel, pásallo a [**PeerGroupAddRecord**](/windows/desktop/api/P2P/nf-p2p-peergroupaddrecord).

## <a name="importing-and-exporting-records"></a>Importar y exportar registros

Los registros de grupo punto a punto se mantienen localmente como una base de datos. Para guardar una instantánea actual de la base de datos de registros del grupo del mismo nivel en un archivo local, llame a [**PeerGroupExportDatabase**](/windows/desktop/api/P2P/nf-p2p-peergroupexportdatabase)y pásele el identificador al grupo del mismo nivel. A continuación, este archivo se puede transportar a otro equipo o aplicación, que puede extraer y usar esta base de datos de registros mediante una llamada a [**PeerGroupImportDatabase**](/windows/desktop/api/P2P/nf-p2p-peergroupimportdatabase).

 

 



