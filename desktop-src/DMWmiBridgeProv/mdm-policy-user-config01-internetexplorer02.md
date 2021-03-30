---
title: Clase MDM_Policy_User_Config01_InternetExplorer02
description: La \_ clase Config01 de usuario de directiva de MDM \_ \_ \_ InternetExplorer02 representa las directivas disponibles de Internet Explorer.
ms.assetid: 2b155e65-5a81-4916-815f-23763759bb9a
keywords:
- Clase MDM_Policy_User_Config01_InternetExplorer02
- MDM_Policy_User_Config01_InternetExplorer02 clase, descrita
topic_type:
- apiref
api_name:
- MDM_Policy_User_Config01_InternetExplorer02
- MDM_Policy_User_Config01_InternetExplorer02.InstanceID
- MDM_Policy_User_Config01_InternetExplorer02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d2f79c00505037508307e93120f9e2545b135678
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104079420"
---
# <a name="mdm_policy_user_config01_internetexplorer02-class"></a><span data-ttu-id="eb9d2-105">\_Clase InternetExplorer02 de usuario de directiva MDM \_ \_ Config01 \_</span><span class="sxs-lookup"><span data-stu-id="eb9d2-105">MDM\_Policy\_User\_Config01\_InternetExplorer02 class</span></span>

<span data-ttu-id="eb9d2-106">\[Algunos datos se relacionan con productos de versiones preliminares que pueden modificarse sustancialmente antes de su lanzamiento comercial.</span><span class="sxs-lookup"><span data-stu-id="eb9d2-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="eb9d2-107">Microsoft no ofrece ninguna garantía, expresa o implícita, con respecto a la información que se ofrece aquí.\]</span><span class="sxs-lookup"><span data-stu-id="eb9d2-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="eb9d2-108">La \_ clase Config01 de usuario de directiva de MDM \_ \_ \_ InternetExplorer02 representa las directivas disponibles de Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="eb9d2-108">The MDM\_Policy\_User\_Config01\_InternetExplorer02 class represents the available Internet Explorer policies.</span></span>

<span data-ttu-id="eb9d2-109">La siguiente sintaxis es código MOF simplificado e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="eb9d2-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="eb9d2-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="eb9d2-110">Syntax</span></span>

``` syntax
[InPartition("local-user"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_User_Config01_InternetExplorer02
{
  string InstanceID;
  string ParentID;
  string AddSearchProvider;
  string AllowActiveXFiltering;
  string AllowAddOnList;
  string AllowDeletingBrowsingHistoryOnExit;
  string AllowCertificateAddressMismatchWarning;
  string AllowAutoComplete;
  string AllowEnhancedProtectedMode;
  string AllowEnterpriseModeFromToolsMenu;
  string AllowEnterpriseModeSiteList;
  string AllowInternetExplorer7PolicyList;
  string AllowInternetExplorerStandardsMode;
  string AllowInternetZoneTemplate;
  string AllowIntranetZoneTemplate;
  string AllowLocalMachineZoneTemplate;
  string AllowLockedDownInternetZoneTemplate;
  string AllowLockedDownIntranetZoneTemplate;
  string AllowLockedDownLocalMachineZoneTemplate;
  string AllowLockedDownRestrictedSitesZoneTemplate;
  string AllowOneWordEntry;
  string AllowSiteToZoneAssignmentList;
  string AllowsLockedDownTrustedSitesZoneTemplate;
  string AllowSoftwareWhenSignatureIsInvalid;
  string AllowsRestrictedSitesZoneTemplate;
  string AllowSuggestedSites;
  string AllowTrustedSitesZoneTemplate;
  string ConsistentMimeHandlingInternetExplorerProcesses;
  string CheckSignaturesOnDownloadedPrograms;
  string CheckServerCertificateRevocation;
  string DisableAdobeFlash;
  string DisableBlockingOfOutdatedActiveXControls;
  string DisableBypassOfSmartScreenWarnings;
  string DisableBypassOfSmartScreenWarningsAboutUncommonFiles;
  string DisableCrashDetection;
  string DisableConfiguringHistory;
  string DisableCustomerExperienceImprovementProgramParticipation;
  string DisableDeletingUserVisitedWebsites;
  string DisableEnclosureDownloading;
  string DisableEncryptionSupport;
  string DisableFirstRunWizard;
  string DisableFlipAheadFeature;
  string DisableHomePageChange;
  string DisableProcessesInEnhancedProtectedMode;
  string DisableInPrivateBrowsing;
  string DisableIgnoringCertificateErrors;
  string DisableProxyChange;
  string DisableSearchProviderChange;
  string DisableSecondaryHomePageChange;
  string DoNotAllowActiveXControlsInProtectedMode;
  string DisableSecuritySettingsCheck;
  string DoNotBlockOutdatedActiveXControls;
  string DoNotBlockOutdatedActiveXControlsOnSpecificDomains;
  string IncludeAllLocalSites;
  string IncludeAllNetworkPaths;
  string InternetZoneAllowAccessToDataSources;
  string InternetZoneAllowAutomaticPromptingForActiveXControls;
  string InternetZoneAllowAutomaticPromptingForFileDownloads;
  string InternetZoneAllowDragAndDropCopyAndPasteFiles;
  string InternetZoneAllowCopyPasteViaScript;
  string InternetZoneAllowFontDownloads;
  string InternetZoneAllowLessPrivilegedSites;
  string InternetZoneAllowLoadingOfXAMLFiles;
  string InternetZoneAllowNETFrameworkReliantComponents;
  string InternetZoneAllowScriptInitiatedWindows;
  string InternetZoneAllowScriptingOfInternetExplorerWebBrowserControls;
  string InternetZoneAllowOnlyApprovedDomainsToUseTDCActiveXControl;
  string InternetZoneAllowOnlyApprovedDomainsToUseActiveXControls;
  string InternetZoneAllowScriptlets;
  string InternetZoneAllowSmartScreenIE;
  string InternetZoneAllowUpdatesToStatusBarViaScript;
  string InternetZoneAllowUserDataPersistence;
  string InternetZoneDoNotRunAntimalwareAgainstActiveXControls;
  string InternetZoneIncludeLocalPathWhenUploadingFilesToServer;
  string InternetZoneEnableProtectedMode;
  string InternetZoneEnableMIMESniffing;
  string InternetZoneEnableDraggingOfContentFromDifferentDomainsWithinWindows;
  string InternetZoneEnableDraggingOfContentFromDifferentDomainsAcrossWindows;
  string InternetZoneEnableCrossSiteScriptingFilter;
  string InternetZoneDownloadUnsignedActiveXControls;
  string InternetZoneDownloadSignedActiveXControls;
  string InternetZoneInitializeAndScriptActiveXControls;
  string InternetZoneJavaPermissions;
  string InternetZoneLogonOptions;
  string InternetZoneLaunchingApplicationsAndFilesInIFRAME;
  string InternetZoneNavigateWindowsAndFrames;
  string InternetZoneWebsitesInLessPrivilegedZonesCanNavigateIntoThisZone;
  string InternetZoneUsePopupBlocker;
  string InternetZoneShowSecurityWarningForPotentiallyUnsafeFiles;
  string InternetZoneRunNETFrameworkReliantComponentsSignedWithAuthenticode;
  string InternetZoneRunNETFrameworkReliantComponentsNotSignedWithAuthenticode;
  string IntranetZoneAllowAccessToDataSources;
  string IntranetZoneAllowAutomaticPromptingForActiveXControls;
  string IntranetZoneAllowAutomaticPromptingForFileDownloads;
  string IntranetZoneAllowFontDownloads;
  string IntranetZoneAllowLessPrivilegedSites;
  string IntranetZoneAllowNETFrameworkReliantComponents;
  string IntranetZoneAllowScriptlets;
  string IntranetZoneAllowSmartScreenIE;
  string IntranetZoneAllowUserDataPersistence;
  string IntranetZoneDoNotRunAntimalwareAgainstActiveXControls;
  string IntranetZoneInitializeAndScriptActiveXControls;
  string IntranetZoneJavaPermissions;
  string IntranetZoneInitializeAndScriptActiveXControlsNotMarkedSafe;
  string IntranetZoneNavigateWindowsAndFrames;
  string LocalMachineZoneAllowAccessToDataSources;
  string LocalMachineZoneAllowAutomaticPromptingForActiveXControls;
  string LocalMachineZoneAllowAutomaticPromptingForFileDownloads;
  string LocalMachineZoneAllowFontDownloads;
  string LocalMachineZoneAllowLessPrivilegedSites;
  string LocalMachineZoneAllowNETFrameworkReliantComponents;
  string LocalMachineZoneAllowScriptlets;
  string LocalMachineZoneAllowSmartScreenIE;
  string LocalMachineZoneAllowUserDataPersistence;
  string LocalMachineZoneDoNotRunAntimalwareAgainstActiveXControls;
  string LocalMachineZoneInitializeAndScriptActiveXControls;
  string LocalMachineZoneJavaPermissions;
  string LocalMachineZoneNavigateWindowsAndFrames;
  string LockedDownInternetZoneAllowAccessToDataSources;
  string LockedDownInternetZoneAllowAutomaticPromptingForActiveXControls;
  string LockedDownInternetZoneAllowAutomaticPromptingForFileDownloads;
  string LockedDownInternetZoneAllowFontDownloads;
  string LockedDownInternetZoneAllowLessPrivilegedSites;
  string LockedDownInternetZoneAllowNETFrameworkReliantComponents;
  string LockedDownInternetZoneAllowScriptlets;
  string LockedDownInternetZoneAllowSmartScreenIE;
  string LockedDownInternetZoneAllowUserDataPersistence;
  string LockedDownInternetZoneInitializeAndScriptActiveXControls;
  string LockedDownInternetZoneJavaPermissions;
  string LockedDownInternetZoneNavigateWindowsAndFrames;
  string LockedDownIntranetZoneAllowAccessToDataSources;
  string LockedDownIntranetZoneAllowAutomaticPromptingForActiveXControls;
  string LockedDownIntranetZoneAllowAutomaticPromptingForFileDownloads;
  string LockedDownIntranetZoneAllowFontDownloads;
  string LockedDownIntranetZoneAllowLessPrivilegedSites;
  string LockedDownIntranetZoneAllowNETFrameworkReliantComponents;
  string LockedDownIntranetZoneAllowScriptlets;
  string LockedDownIntranetZoneAllowSmartScreenIE;
  string LockedDownIntranetZoneAllowUserDataPersistence;
  string LockedDownIntranetZoneInitializeAndScriptActiveXControls;
  string LockedDownIntranetZoneNavigateWindowsAndFrames;
  string LockedDownLocalMachineZoneAllowAccessToDataSources;
  string LockedDownLocalMachineZoneAllowAutomaticPromptingForActiveXControls;
  string LockedDownLocalMachineZoneAllowAutomaticPromptingForFileDownloads;
  string LockedDownLocalMachineZoneAllowFontDownloads;
  string LockedDownLocalMachineZoneAllowLessPrivilegedSites;
  string LockedDownLocalMachineZoneAllowNETFrameworkReliantComponents;
  string LockedDownLocalMachineZoneAllowScriptlets;
  string LockedDownLocalMachineZoneAllowSmartScreenIE;
  string LockedDownLocalMachineZoneAllowUserDataPersistence;
  string LockedDownLocalMachineZoneInitializeAndScriptActiveXControls;
  string LockedDownLocalMachineZoneJavaPermissions;
  string LockedDownLocalMachineZoneNavigateWindowsAndFrames;
  string LockedDownRestrictedSitesZoneAllowAccessToDataSources;
  string LockedDownRestrictedSitesZoneAllowAutomaticPromptingForActiveXControls;
  string LockedDownRestrictedSitesZoneAllowAutomaticPromptingForFileDownloads;
  string LockedDownRestrictedSitesZoneAllowFontDownloads;
  string LockedDownRestrictedSitesZoneAllowLessPrivilegedSites;
  string LockedDownRestrictedSitesZoneAllowNETFrameworkReliantComponents;
  string LockedDownRestrictedSitesZoneAllowScriptlets;
  string LockedDownRestrictedSitesZoneAllowSmartScreenIE;
  string LockedDownRestrictedSitesZoneAllowUserDataPersistence;
  string LockedDownRestrictedSitesZoneInitializeAndScriptActiveXControls;
  string LockedDownRestrictedSitesZoneJavaPermissions;
  string LockedDownRestrictedSitesZoneNavigateWindowsAndFrames;
  string LockedDownTrustedSitesZoneAllowAccessToDataSources;
  string LockedDownTrustedSitesZoneAllowAutomaticPromptingForActiveXControls;
  string LockedDownTrustedSitesZoneAllowAutomaticPromptingForFileDownloads;
  string LockedDownTrustedSitesZoneAllowFontDownloads;
  string LockedDownTrustedSitesZoneAllowLessPrivilegedSites;
  string LockedDownTrustedSitesZoneAllowNETFrameworkReliantComponents;
  string LockedDownTrustedSitesZoneAllowScriptlets;
  string LockedDownTrustedSitesZoneAllowSmartScreenIE;
  string LockedDownTrustedSitesZoneAllowUserDataPersistence;
  string LockedDownTrustedSitesZoneInitializeAndScriptActiveXControls;
  string LockedDownTrustedSitesZoneJavaPermissions;
  string LockedDownTrustedSitesZoneNavigateWindowsAndFrames;
  string RestrictActiveXInstallInternetExplorerProcesses;
  string RemoveRunThisTimeButtonForOutdatedActiveXControls;
  string ProtectionFromZoneElevationInternetExplorerProcesses;
  string PreventPerUserInstallationOfActiveXControls;
  string PreventManagingSmartScreenFilter;
  string NotificationBarInternetExplorerProcesses;
  string MKProtocolSecurityRestrictionInternetExplorerProcesses;
  string MimeSniffingSafetyFeatureInternetExplorerProcesses;
  string RestrictedSitesZoneAllowAccessToDataSources;
  string RestrictedSitesZoneAllowActiveScripting;
  string RestrictedSitesZoneAllowAutomaticPromptingForActiveXControls;
  string RestrictedSitesZoneAllowAutomaticPromptingForFileDownloads;
  string RestrictedSitesZoneAllowFileDownloads;
  string RestrictedSitesZoneAllowDragAndDropCopyAndPasteFiles;
  string RestrictedSitesZoneAllowCopyPasteViaScript;
  string RestrictedSitesZoneAllowBinaryAndScriptBehaviors;
  string RestrictedSitesZoneAllowFontDownloads;
  string RestrictedSitesZoneAllowLessPrivilegedSites;
  string RestrictedSitesZoneAllowMETAREFRESH;
  string RestrictedSitesZoneAllowLoadingOfXAMLFiles;
  string RestrictedSitesZoneAllowNETFrameworkReliantComponents;
  string RestrictedSitesZoneAllowScriptInitiatedWindows;
  string RestrictedSitesZoneAllowScriptingOfInternetExplorerWebBrowserControls;
  string RestrictedSitesZoneAllowOnlyApprovedDomainsToUseTDCActiveXControl;
  string RestrictedSitesZoneAllowOnlyApprovedDomainsToUseActiveXControls;
  string RestrictedSitesZoneAllowScriptlets;
  string RestrictedSitesZoneAllowSmartScreenIE;
  string RestrictedSitesZoneAllowUpdatesToStatusBarViaScript;
  string RestrictedSitesZoneAllowUserDataPersistence;
  string RestrictedSitesZoneIncludeLocalPathWhenUploadingFilesToServer;
  string RestrictedSitesZoneEnableMIMESniffing;
  string RestrictedSitesZoneEnableDraggingOfContentFromDifferentDomainsWithinWindows;
  string RestrictedSitesZoneEnableDraggingOfContentFromDifferentDomainsAcrossWindows;
  string RestrictedSitesZoneDownloadUnsignedActiveXControls;
  string RestrictedSitesZoneEnableCrossSiteScriptingFilter;
  string RestrictedSitesZoneDownloadSignedActiveXControls;
  string RestrictedSitesZoneDoNotRunAntimalwareAgainstActiveXControls;
  string RestrictedSitesZoneInitializeAndScriptActiveXControls;
  string RestrictedSitesZoneLogonOptions;
  string RestrictedSitesZoneLaunchingApplicationsAndFilesInIFRAME;
  string RestrictedSitesZoneJavaPermissions;
  string RestrictedSitesZoneNavigateWindowsAndFrames;
  string ScriptedWindowSecurityRestrictionsInternetExplorerProcesses;
  string RestrictFileDownloadInternetExplorerProcesses;
  string RestrictedSitesZoneScriptActiveXControlsMarkedSafeForScripting;
  string RestrictedSitesZoneUsePopupBlocker;
  string RestrictedSitesZoneTurnOnProtectedMode;
  string RestrictedSitesZoneTurnOnCrossSiteScriptingFilter;
  string RestrictedSitesZoneShowSecurityWarningForPotentiallyUnsafeFiles;
  string RestrictedSitesZoneScriptingOfJavaApplets;
  string RestrictedSitesZoneRunNETFrameworkReliantComponentsSignedWithAuthenticode;
  string RestrictedSitesZoneRunActiveXControlsAndPlugins;
  string RestrictedSitesZoneNavigateWindowsAndFramesAcrossDomains;
  string SearchProviderList;
  string SpecifyUseOfActiveXInstallerService;
  string TrustedSitesZoneAllowAccessToDataSources;
  string TrustedSitesZoneAllowAutomaticPromptingForActiveXControls;
  string TrustedSitesZoneAllowAutomaticPromptingForFileDownloads;
  string TrustedSitesZoneAllowFontDownloads;
  string TrustedSitesZoneAllowLessPrivilegedSites;
  string TrustedSitesZoneAllowNETFrameworkReliantComponents;
  string TrustedSitesZoneAllowScriptlets;
  string TrustedSitesZoneAllowSmartScreenIE;
  string TrustedSitesZoneAllowUserDataPersistence;
  string TrustedSitesZoneDontRunAntimalwareProgramsAgainstActiveXControls;
  string TrustedSitesZoneDoNotRunAntimalwareAgainstActiveXControls;
  string TrustedSitesZoneInitializeAndScriptActiveXControls;
  string TrustedSitesZoneInitializeAndScriptActiveXControlsNotMarkedSafe;
  string TrustedSitesZoneInitializeAndScriptActiveXControlsNotMarkedAsSafe;
  string TrustedSitesZoneJavaPermissions;
  string TrustedSitesZoneNavigateWindowsAndFrames;
};
```

## <a name="members"></a><span data-ttu-id="eb9d2-111">Miembros</span><span class="sxs-lookup"><span data-stu-id="eb9d2-111">Members</span></span>

<span data-ttu-id="eb9d2-112">La clase Config01 de usuario de la **\_ Directiva MDM \_ \_ \_ InternetExplorer02** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="eb9d2-112">The **MDM\_Policy\_User\_Config01\_InternetExplorer02** class has these types of members:</span></span>

-   [<span data-ttu-id="eb9d2-113">Propiedades</span><span class="sxs-lookup"><span data-stu-id="eb9d2-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="eb9d2-114">Propiedades</span><span class="sxs-lookup"><span data-stu-id="eb9d2-114">Properties</span></span>

<span data-ttu-id="eb9d2-115">La clase Config01 de usuario de la **\_ Directiva MDM \_ \_ \_ InternetExplorer02** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="eb9d2-115">The **MDM\_Policy\_User\_Config01\_InternetExplorer02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="eb9d2-116">AddSearchProvider</span><span class="sxs-lookup"><span data-stu-id="eb9d2-116">AddSearchProvider</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-addsearchprovider)
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb9d2-117">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="eb9d2-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="eb9d2-118">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="eb9d2-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="eb9d2-119">AllowActiveXFiltering</span><span class="sxs-lookup"><span data-stu-id="eb9d2-119">AllowActiveXFiltering</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowactivexfiltering)
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb9d2-120">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="eb9d2-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="eb9d2-121">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="eb9d2-121">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="eb9d2-122">AllowAddOnList</span><span class="sxs-lookup"><span data-stu-id="eb9d2-122">AllowAddOnList</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowaddonlist)
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb9d2-123">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="eb9d2-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="eb9d2-124">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="eb9d2-124">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="eb9d2-125">AllowAutoComplete</span><span class="sxs-lookup"><span data-stu-id="eb9d2-125">AllowAutoComplete</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowautocomplete)
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb9d2-126">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="eb9d2-126">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="eb9d2-127">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="eb9d2-127">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="eb9d2-128">AllowCertificateAddressMismatchWarning</span><span class="sxs-lookup"><span data-stu-id="eb9d2-128">AllowCertificateAddressMismatchWarning</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowcertificateaddressmismatchwarning)
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb9d2-129">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="eb9d2-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="eb9d2-130">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="eb9d2-130">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="eb9d2-131">AllowDeletingBrowsingHistoryOnExit</span><span class="sxs-lookup"><span data-stu-id="eb9d2-131">AllowDeletingBrowsingHistoryOnExit</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowdeletingbrowsinghistoryonexit)
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb9d2-132">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="eb9d2-132">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="eb9d2-133">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="eb9d2-133">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="eb9d2-134">AllowEnhancedProtectedMode</span><span class="sxs-lookup"><span data-stu-id="eb9d2-134">AllowEnhancedProtectedMode</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowenhancedprotectedmode)
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb9d2-135">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="eb9d2-135">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="eb9d2-136">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="eb9d2-136">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="eb9d2-137">AllowEnterpriseModeFromToolsMenu</span><span class="sxs-lookup"><span data-stu-id="eb9d2-137">AllowEnterpriseModeFromToolsMenu</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowenterprisemodefromtoolsmenu)
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb9d2-138">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="eb9d2-138">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="eb9d2-139">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="eb9d2-139">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="eb9d2-140">AllowEnterpriseModeSiteList</span><span class="sxs-lookup"><span data-stu-id="eb9d2-140">AllowEnterpriseModeSiteList</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowenterprisemodesitelist)
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb9d2-141">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="eb9d2-141">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="eb9d2-142">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="eb9d2-142">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="eb9d2-143">AllowInternetExplorer7PolicyList</span><span class="sxs-lookup"><span data-stu-id="eb9d2-143">AllowInternetExplorer7PolicyList</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowinternetexplorer7policylist)
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb9d2-144">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="eb9d2-144">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="eb9d2-145">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="eb9d2-145">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="eb9d2-146">AllowInternetExplorerStandardsMode</span><span class="sxs-lookup"><span data-stu-id="eb9d2-146">AllowInternetExplorerStandardsMode</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowinternetexplorerstandardsmode)
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb9d2-147">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="eb9d2-147">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="eb9d2-148">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="eb9d2-148">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="eb9d2-149">AllowInternetZoneTemplate</span><span class="sxs-lookup"><span data-stu-id="eb9d2-149">AllowInternetZoneTemplate</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowinternetzonetemplate)
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb9d2-150">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="eb9d2-150">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="eb9d2-151">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="eb9d2-151">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="eb9d2-152">AllowIntranetZoneTemplate</span><span class="sxs-lookup"><span data-stu-id="eb9d2-152">AllowIntranetZoneTemplate</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowintranetzonetemplate)
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb9d2-153">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="eb9d2-153">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="eb9d2-154">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="eb9d2-154">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="eb9d2-155">AllowLocalMachineZoneTemplate</span><span class="sxs-lookup"><span data-stu-id="eb9d2-155">AllowLocalMachineZoneTemplate</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowlocalmachinezonetemplate)
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb9d2-156">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="eb9d2-156">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="eb9d2-157">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="eb9d2-157">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="eb9d2-158">AllowLockedDownInternetZoneTemplate</span><span class="sxs-lookup"><span data-stu-id="eb9d2-158">AllowLockedDownInternetZoneTemplate</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowlockeddowninternetzonetemplate)
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb9d2-159">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="eb9d2-159">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="eb9d2-160">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="eb9d2-160">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="eb9d2-161">AllowLockedDownIntranetZoneTemplate</span><span class="sxs-lookup"><span data-stu-id="eb9d2-161">AllowLockedDownIntranetZoneTemplate</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowlockeddownintranetzonetemplate)
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb9d2-162">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="eb9d2-162">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="eb9d2-163">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="eb9d2-163">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="eb9d2-164">AllowLockedDownLocalMachineZoneTemplate</span><span class="sxs-lookup"><span data-stu-id="eb9d2-164">AllowLockedDownLocalMachineZoneTemplate</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowlockeddownlocalmachinezonetemplate)
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb9d2-165">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="eb9d2-165">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="eb9d2-166">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="eb9d2-166">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="eb9d2-167">AllowLockedDownRestrictedSitesZoneTemplate</span><span class="sxs-lookup"><span data-stu-id="eb9d2-167">AllowLockedDownRestrictedSitesZoneTemplate</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowlockeddownrestrictedsiteszonetemplate)
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb9d2-168">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="eb9d2-168">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="eb9d2-169">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="eb9d2-169">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="eb9d2-170">AllowOneWordEntry</span><span class="sxs-lookup"><span data-stu-id="eb9d2-170">AllowOneWordEntry</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowonewordentry)
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb9d2-171">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="eb9d2-171">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="eb9d2-172">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="eb9d2-172">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="eb9d2-173">AllowSiteToZoneAssignmentList</span><span class="sxs-lookup"><span data-stu-id="eb9d2-173">AllowSiteToZoneAssignmentList</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowsitetozoneassignmentlist)
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb9d2-174">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="eb9d2-174">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="eb9d2-175">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="eb9d2-175">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="eb9d2-176">AllowsLockedDownTrustedSitesZoneTemplate</span><span class="sxs-lookup"><span data-stu-id="eb9d2-176">AllowsLockedDownTrustedSitesZoneTemplate</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowslockeddowntrustedsiteszonetemplate)
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb9d2-177">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="eb9d2-177">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="eb9d2-178">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="eb9d2-178">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="eb9d2-179">AllowSoftwareWhenSignatureIsInvalid</span><span class="sxs-lookup"><span data-stu-id="eb9d2-179">AllowSoftwareWhenSignatureIsInvalid</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowsoftwarewhensignatureisinvalid)
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb9d2-180">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="eb9d2-180">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="eb9d2-181">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="eb9d2-181">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="eb9d2-182">AllowsRestrictedSitesZoneTemplate</span><span class="sxs-lookup"><span data-stu-id="eb9d2-182">AllowsRestrictedSitesZoneTemplate</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowsrestrictedsiteszonetemplate)
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb9d2-183">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="eb9d2-183">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="eb9d2-184">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="eb9d2-184">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="eb9d2-185">AllowSuggestedSites</span><span class="sxs-lookup"><span data-stu-id="eb9d2-185">AllowSuggestedSites</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowsuggestedsites)
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb9d2-186">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="eb9d2-186">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="eb9d2-187">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="eb9d2-187">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="eb9d2-188">AllowTrustedSitesZoneTemplate</span><span class="sxs-lookup"><span data-stu-id="eb9d2-188">AllowTrustedSitesZoneTemplate</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowtrustedsiteszonetemplate)
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb9d2-189">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="eb9d2-189">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="eb9d2-190">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="eb9d2-190">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="eb9d2-191">CheckServerCertificateRevocation</span><span class="sxs-lookup"><span data-stu-id="eb9d2-191">CheckServerCertificateRevocation</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-checkservercertificaterevocation)
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb9d2-192">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="eb9d2-192">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="eb9d2-193">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="eb9d2-193">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="eb9d2-194">CheckSignaturesOnDownloadedPrograms</span><span class="sxs-lookup"><span data-stu-id="eb9d2-194">CheckSignaturesOnDownloadedPrograms</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-checksignaturesondownloadedprograms)
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb9d2-195">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="eb9d2-195">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="eb9d2-196">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="eb9d2-196">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="eb9d2-197">ConsistentMimeHandlingInternetExplorerProcesses</span><span class="sxs-lookup"><span data-stu-id="eb9d2-197">ConsistentMimeHandlingInternetExplorerProcesses</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-consistentmimehandlinginternetexplorerprocesses)
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb9d2-198">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="eb9d2-198">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="eb9d2-199">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="eb9d2-199">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="eb9d2-200">DisableAdobeFlash</span><span class="sxs-lookup"><span data-stu-id="eb9d2-200">DisableAdobeFlash</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-disableadobeflash)
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb9d2-201">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="eb9d2-201">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="eb9d2-202">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="eb9d2-202">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="eb9d2-203">DisableBlockingOfOutdatedActiveXControls</span><span class="sxs-lookup"><span data-stu-id="eb9d2-203">DisableBlockingOfOutdatedActiveXControls</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb9d2-204">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="eb9d2-204">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="eb9d2-205">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="eb9d2-205">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="eb9d2-206">DisableBypassOfSmartScreenWarnings</span><span class="sxs-lookup"><span data-stu-id="eb9d2-206">DisableBypassOfSmartScreenWarnings</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-disablebypassofsmartscreenwarnings)
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb9d2-207">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="eb9d2-207">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="eb9d2-208">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="eb9d2-208">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="eb9d2-209">DisableBypassOfSmartScreenWarningsAboutUncommonFiles</span><span class="sxs-lookup"><span data-stu-id="eb9d2-209">DisableBypassOfSmartScreenWarningsAboutUncommonFiles</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-disablebypassofsmartscreenwarningsaboutuncommonfiles)
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb9d2-210">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="eb9d2-210">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="eb9d2-211">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="eb9d2-211">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="eb9d2-212">DisableConfiguringHistory</span><span class="sxs-lookup"><span data-stu-id="eb9d2-212">DisableConfiguringHistory</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-disableconfiguringhistory)
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb9d2-213">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="eb9d2-213">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="eb9d2-214">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="eb9d2-214">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="eb9d2-215">DisableCrashDetection</span><span class="sxs-lookup"><span data-stu-id="eb9d2-215">DisableCrashDetection</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-disablecrashdetection)
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb9d2-216">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="eb9d2-216">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="eb9d2-217">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="eb9d2-217">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="eb9d2-218">DisableCustomerExperienceImprovementProgramParticipation</span><span class="sxs-lookup"><span data-stu-id="eb9d2-218">DisableCustomerExperienceImprovementProgramParticipation</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-disablecustomerexperienceimprovementprogramparticipation)
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb9d2-219">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="eb9d2-219">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="eb9d2-220">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="eb9d2-220">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="eb9d2-221">DisableDeletingUserVisitedWebsites</span><span class="sxs-lookup"><span data-stu-id="eb9d2-221">DisableDeletingUserVisitedWebsites</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-disabledeletinguservisitedwebsites)
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb9d2-222">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="eb9d2-222">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="eb9d2-223">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="eb9d2-223">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="eb9d2-224">DisableEnclosureDownloading</span><span class="sxs-lookup"><span data-stu-id="eb9d2-224">DisableEnclosureDownloading</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-disableenclosuredownloading)
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb9d2-225">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="eb9d2-225">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="eb9d2-226">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="eb9d2-226">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="eb9d2-227">DisableEncryptionSupport</span><span class="sxs-lookup"><span data-stu-id="eb9d2-227">DisableEncryptionSupport</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-disableencryptionsupport)
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb9d2-228">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="eb9d2-228">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="eb9d2-229">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="eb9d2-229">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="eb9d2-230">DisableFirstRunWizard</span><span class="sxs-lookup"><span data-stu-id="eb9d2-230">DisableFirstRunWizard</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-disablefirstrunwizard)
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb9d2-231">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="eb9d2-231">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="eb9d2-232">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="eb9d2-232">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="eb9d2-233">DisableFlipAheadFeature</span><span class="sxs-lookup"><span data-stu-id="eb9d2-233">DisableFlipAheadFeature</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-disableflipaheadfeature)
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb9d2-234">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="eb9d2-234">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="eb9d2-235">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="eb9d2-235">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="eb9d2-236">DisableHomePageChange</span><span class="sxs-lookup"><span data-stu-id="eb9d2-236">DisableHomePageChange</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-disablehomepagechange)
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb9d2-237">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="eb9d2-237">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="eb9d2-238">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="eb9d2-238">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="eb9d2-239">DisableIgnoringCertificateErrors</span><span class="sxs-lookup"><span data-stu-id="eb9d2-239">DisableIgnoringCertificateErrors</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-disableignoringcertificateerrors)
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb9d2-240">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="eb9d2-240">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="eb9d2-241">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="eb9d2-241">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="eb9d2-242">DisableInPrivateBrowsing</span><span class="sxs-lookup"><span data-stu-id="eb9d2-242">DisableInPrivateBrowsing</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-disableinprivatebrowsing)
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb9d2-243">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="eb9d2-243">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="eb9d2-244">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="eb9d2-244">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="eb9d2-245">DisableProcessesInEnhancedProtectedMode</span><span class="sxs-lookup"><span data-stu-id="eb9d2-245">DisableProcessesInEnhancedProtectedMode</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-disableprocessesinenhancedprotectedmode)
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb9d2-246">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="eb9d2-246">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="eb9d2-247">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="eb9d2-247">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="eb9d2-248">DisableProxyChange</span><span class="sxs-lookup"><span data-stu-id="eb9d2-248">DisableProxyChange</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-disableproxychange)
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb9d2-249">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="eb9d2-249">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="eb9d2-250">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="eb9d2-250">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="eb9d2-251">DisableSearchProviderChange</span><span class="sxs-lookup"><span data-stu-id="eb9d2-251">DisableSearchProviderChange</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-disablesearchproviderchange)
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb9d2-252">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="eb9d2-252">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="eb9d2-253">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="eb9d2-253">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="eb9d2-254">DisableSecondaryHomePageChange</span><span class="sxs-lookup"><span data-stu-id="eb9d2-254">DisableSecondaryHomePageChange</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-disablesecondaryhomepagechange)
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb9d2-255">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="eb9d2-255">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="eb9d2-256">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="eb9d2-256">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="eb9d2-257">DisableSecuritySettingsCheck</span><span class="sxs-lookup"><span data-stu-id="eb9d2-257">DisableSecuritySettingsCheck</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-disablesecuritysettingscheck)
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb9d2-258">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="eb9d2-258">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="eb9d2-259">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="eb9d2-259">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="eb9d2-260">DoNotAllowActiveXControlsInProtectedMode</span><span class="sxs-lookup"><span data-stu-id="eb9d2-260">DoNotAllowActiveXControlsInProtectedMode</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-donotallowactivexcontrolsinprotectedmode)
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb9d2-261">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="eb9d2-261">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="eb9d2-262">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="eb9d2-262">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="eb9d2-263">DoNotBlockOutdatedActiveXControls</span><span class="sxs-lookup"><span data-stu-id="eb9d2-263">DoNotBlockOutdatedActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-donotblockoutdatedactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb9d2-264">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="eb9d2-264">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="eb9d2-265">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="eb9d2-265">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="eb9d2-266">DoNotBlockOutdatedActiveXControlsOnSpecificDomains</span><span class="sxs-lookup"><span data-stu-id="eb9d2-266">DoNotBlockOutdatedActiveXControlsOnSpecificDomains</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-donotblockoutdatedactivexcontrolsonspecificdomains)
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb9d2-267">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="eb9d2-267">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="eb9d2-268">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="eb9d2-268">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="eb9d2-269">IncludeAllLocalSites</span><span class="sxs-lookup"><span data-stu-id="eb9d2-269">IncludeAllLocalSites</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-includealllocalsites)
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb9d2-270">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="eb9d2-270">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="eb9d2-271">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="eb9d2-271">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="eb9d2-272">IncludeAllNetworkPaths</span><span class="sxs-lookup"><span data-stu-id="eb9d2-272">IncludeAllNetworkPaths</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-includeallnetworkpaths)
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb9d2-273">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="eb9d2-273">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="eb9d2-274">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="eb9d2-274">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="eb9d2-275">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="eb9d2-275">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb9d2-276">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="eb9d2-276">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="eb9d2-277">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="eb9d2-277">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="eb9d2-278">Calificadores: [ **clave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="eb9d2-278">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="eb9d2-279">InternetZoneAllowAccessToDataSources</span><span class="sxs-lookup"><span data-stu-id="eb9d2-279">InternetZoneAllowAccessToDataSources</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneallowaccesstodatasources)
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb9d2-280">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="eb9d2-280">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="eb9d2-281">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="eb9d2-281">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="eb9d2-282">InternetZoneAllowAutomaticPromptingForActiveXControls</span><span class="sxs-lookup"><span data-stu-id="eb9d2-282">InternetZoneAllowAutomaticPromptingForActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneallowautomaticpromptingforactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb9d2-283">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="eb9d2-283">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="eb9d2-284">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="eb9d2-284">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="eb9d2-285">InternetZoneAllowAutomaticPromptingForFileDownloads</span><span class="sxs-lookup"><span data-stu-id="eb9d2-285">InternetZoneAllowAutomaticPromptingForFileDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneallowautomaticpromptingforfiledownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb9d2-286">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="eb9d2-286">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="eb9d2-287">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="eb9d2-287">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="eb9d2-288">InternetZoneAllowCopyPasteViaScript</span><span class="sxs-lookup"><span data-stu-id="eb9d2-288">InternetZoneAllowCopyPasteViaScript</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneallowcopypasteviascript)
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb9d2-289">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="eb9d2-289">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="eb9d2-290">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="eb9d2-290">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="eb9d2-291">InternetZoneAllowDragAndDropCopyAndPasteFiles</span><span class="sxs-lookup"><span data-stu-id="eb9d2-291">InternetZoneAllowDragAndDropCopyAndPasteFiles</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneallowdraganddropcopyandpastefiles)
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb9d2-292">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="eb9d2-292">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="eb9d2-293">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="eb9d2-293">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="eb9d2-294">InternetZoneAllowFontDownloads</span><span class="sxs-lookup"><span data-stu-id="eb9d2-294">InternetZoneAllowFontDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneallowfontdownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb9d2-295">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="eb9d2-295">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="eb9d2-296">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="eb9d2-296">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="eb9d2-297">InternetZoneAllowLessPrivilegedSites</span><span class="sxs-lookup"><span data-stu-id="eb9d2-297">InternetZoneAllowLessPrivilegedSites</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneallowlessprivilegedsites)
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb9d2-298">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="eb9d2-298">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="eb9d2-299">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="eb9d2-299">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="eb9d2-300">InternetZoneAllowLoadingOfXAMLFiles</span><span class="sxs-lookup"><span data-stu-id="eb9d2-300">InternetZoneAllowLoadingOfXAMLFiles</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneallowloadingofxamlfiles)
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb9d2-301">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="eb9d2-301">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="eb9d2-302">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="eb9d2-302">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="eb9d2-303">InternetZoneAllowNETFrameworkReliantComponents</span><span class="sxs-lookup"><span data-stu-id="eb9d2-303">InternetZoneAllowNETFrameworkReliantComponents</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneallownetframeworkreliantcomponents)
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb9d2-304">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="eb9d2-304">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="eb9d2-305">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="eb9d2-305">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="eb9d2-306">InternetZoneAllowOnlyApprovedDomainsToUseActiveXControls</span><span class="sxs-lookup"><span data-stu-id="eb9d2-306">InternetZoneAllowOnlyApprovedDomainsToUseActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneallowonlyapproveddomainstouseactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb9d2-307">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="eb9d2-307">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="eb9d2-308">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="eb9d2-308">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="eb9d2-309">InternetZoneAllowOnlyApprovedDomainsToUseTDCActiveXControl</span><span class="sxs-lookup"><span data-stu-id="eb9d2-309">InternetZoneAllowOnlyApprovedDomainsToUseTDCActiveXControl</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneallowonlyapproveddomainstousetdcactivexcontrol)
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb9d2-310">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="eb9d2-310">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="eb9d2-311">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="eb9d2-311">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="eb9d2-312">InternetZoneAllowScriptingOfInternetExplorerWebBrowserControls</span><span class="sxs-lookup"><span data-stu-id="eb9d2-312">InternetZoneAllowScriptingOfInternetExplorerWebBrowserControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneallowscriptingofinternetexplorerwebbrowsercontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb9d2-313">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="eb9d2-313">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="eb9d2-314">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="eb9d2-314">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="eb9d2-315">InternetZoneAllowScriptInitiatedWindows</span><span class="sxs-lookup"><span data-stu-id="eb9d2-315">InternetZoneAllowScriptInitiatedWindows</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneallowscriptinitiatedwindows)
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb9d2-316">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="eb9d2-316">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="eb9d2-317">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="eb9d2-317">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="eb9d2-318">InternetZoneAllowScriptlets</span><span class="sxs-lookup"><span data-stu-id="eb9d2-318">InternetZoneAllowScriptlets</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneallowscriptlets)
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb9d2-319">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="eb9d2-319">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="eb9d2-320">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="eb9d2-320">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="eb9d2-321">InternetZoneAllowSmartScreenIE</span><span class="sxs-lookup"><span data-stu-id="eb9d2-321">InternetZoneAllowSmartScreenIE</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneallowsmartscreenie)
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb9d2-322">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="eb9d2-322">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="eb9d2-323">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="eb9d2-323">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="eb9d2-324">InternetZoneAllowUpdatesToStatusBarViaScript</span><span class="sxs-lookup"><span data-stu-id="eb9d2-324">InternetZoneAllowUpdatesToStatusBarViaScript</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneallowupdatestostatusbarviascript)
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb9d2-325">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="eb9d2-325">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="eb9d2-326">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="eb9d2-326">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="eb9d2-327">InternetZoneAllowUserDataPersistence</span><span class="sxs-lookup"><span data-stu-id="eb9d2-327">InternetZoneAllowUserDataPersistence</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneallowuserdatapersistence)
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb9d2-328">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="eb9d2-328">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="eb9d2-329">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="eb9d2-329">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="eb9d2-330">InternetZoneDoNotRunAntimalwareAgainstActiveXControls</span><span class="sxs-lookup"><span data-stu-id="eb9d2-330">InternetZoneDoNotRunAntimalwareAgainstActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzonedonotrunantimalwareagainstactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb9d2-331">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="eb9d2-331">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="eb9d2-332">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="eb9d2-332">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="eb9d2-333">InternetZoneDownloadSignedActiveXControls</span><span class="sxs-lookup"><span data-stu-id="eb9d2-333">InternetZoneDownloadSignedActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzonedownloadsignedactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb9d2-334">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="eb9d2-334">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="eb9d2-335">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="eb9d2-335">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="eb9d2-336">InternetZoneDownloadUnsignedActiveXControls</span><span class="sxs-lookup"><span data-stu-id="eb9d2-336">InternetZoneDownloadUnsignedActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzonedownloadunsignedactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb9d2-337">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="eb9d2-337">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="eb9d2-338">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="eb9d2-338">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="eb9d2-339">InternetZoneEnableCrossSiteScriptingFilter</span><span class="sxs-lookup"><span data-stu-id="eb9d2-339">InternetZoneEnableCrossSiteScriptingFilter</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneenablecrosssitescriptingfilter)
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb9d2-340">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="eb9d2-340">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="eb9d2-341">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="eb9d2-341">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="eb9d2-342">InternetZoneEnableDraggingOfContentFromDifferentDomainsAcrossWindows</span><span class="sxs-lookup"><span data-stu-id="eb9d2-342">InternetZoneEnableDraggingOfContentFromDifferentDomainsAcrossWindows</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneenabledraggingofcontentfromdifferentdomainsacrosswindows)
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb9d2-343">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="eb9d2-343">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="eb9d2-344">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="eb9d2-344">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="eb9d2-345">InternetZoneEnableDraggingOfContentFromDifferentDomainsWithinWindows</span><span class="sxs-lookup"><span data-stu-id="eb9d2-345">InternetZoneEnableDraggingOfContentFromDifferentDomainsWithinWindows</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneenabledraggingofcontentfromdifferentdomainswithinwindows)
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb9d2-346">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="eb9d2-346">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="eb9d2-347">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="eb9d2-347">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="eb9d2-348">InternetZoneEnableMIMESniffing</span><span class="sxs-lookup"><span data-stu-id="eb9d2-348">InternetZoneEnableMIMESniffing</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneenablemimesniffing)
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb9d2-349">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="eb9d2-349">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="eb9d2-350">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="eb9d2-350">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="eb9d2-351">InternetZoneEnableProtectedMode</span><span class="sxs-lookup"><span data-stu-id="eb9d2-351">InternetZoneEnableProtectedMode</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneenableprotectedmode)
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb9d2-352">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="eb9d2-352">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="eb9d2-353">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="eb9d2-353">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="eb9d2-354">InternetZoneIncludeLocalPathWhenUploadingFilesToServer</span><span class="sxs-lookup"><span data-stu-id="eb9d2-354">InternetZoneIncludeLocalPathWhenUploadingFilesToServer</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneincludelocalpathwhenuploadingfilestoserver)
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb9d2-355">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="eb9d2-355">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="eb9d2-356">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="eb9d2-356">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="eb9d2-357">InternetZoneInitializeAndScriptActiveXControls</span><span class="sxs-lookup"><span data-stu-id="eb9d2-357">InternetZoneInitializeAndScriptActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneinitializeandscriptactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb9d2-358">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="eb9d2-358">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="eb9d2-359">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="eb9d2-359">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="eb9d2-360">InternetZoneJavaPermissions</span><span class="sxs-lookup"><span data-stu-id="eb9d2-360">InternetZoneJavaPermissions</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzonejavapermissions)
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb9d2-361">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="eb9d2-361">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="eb9d2-362">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="eb9d2-362">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="eb9d2-363">InternetZoneLaunchingApplicationsAndFilesInIFRAME</span><span class="sxs-lookup"><span data-stu-id="eb9d2-363">InternetZoneLaunchingApplicationsAndFilesInIFRAME</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzonelaunchingapplicationsandfilesiniframe)
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb9d2-364">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="eb9d2-364">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="eb9d2-365">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="eb9d2-365">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="eb9d2-366">InternetZoneLogonOptions</span><span class="sxs-lookup"><span data-stu-id="eb9d2-366">InternetZoneLogonOptions</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzonelogonoptions)
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb9d2-367">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="eb9d2-367">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="eb9d2-368">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="eb9d2-368">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="eb9d2-369">InternetZoneNavigateWindowsAndFrames</span><span class="sxs-lookup"><span data-stu-id="eb9d2-369">InternetZoneNavigateWindowsAndFrames</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzonenavigatewindowsandframes)
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb9d2-370">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="eb9d2-370">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="eb9d2-371">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="eb9d2-371">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="eb9d2-372">InternetZoneRunNETFrameworkReliantComponentsNotSignedWithAuthenticode</span><span class="sxs-lookup"><span data-stu-id="eb9d2-372">InternetZoneRunNETFrameworkReliantComponentsNotSignedWithAuthenticode</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb9d2-373">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="eb9d2-373">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="eb9d2-374">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="eb9d2-374">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="eb9d2-375">InternetZoneRunNETFrameworkReliantComponentsSignedWithAuthenticode</span><span class="sxs-lookup"><span data-stu-id="eb9d2-375">InternetZoneRunNETFrameworkReliantComponentsSignedWithAuthenticode</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzonerunnetframeworkreliantcomponentssignedwithauthenticode)
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb9d2-376">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="eb9d2-376">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="eb9d2-377">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="eb9d2-377">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="eb9d2-378">InternetZoneShowSecurityWarningForPotentiallyUnsafeFiles</span><span class="sxs-lookup"><span data-stu-id="eb9d2-378">InternetZoneShowSecurityWarningForPotentiallyUnsafeFiles</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneshowsecuritywarningforpotentiallyunsafefiles)
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb9d2-379">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="eb9d2-379">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="eb9d2-380">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="eb9d2-380">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="eb9d2-381">InternetZoneUsePopupBlocker</span><span class="sxs-lookup"><span data-stu-id="eb9d2-381">InternetZoneUsePopupBlocker</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneusepopupblocker)
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb9d2-382">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="eb9d2-382">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="eb9d2-383">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="eb9d2-383">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="eb9d2-384">InternetZoneWebsitesInLessPrivilegedZonesCanNavigateIntoThisZone</span><span class="sxs-lookup"><span data-stu-id="eb9d2-384">InternetZoneWebsitesInLessPrivilegedZonesCanNavigateIntoThisZone</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb9d2-385">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="eb9d2-385">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="eb9d2-386">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="eb9d2-386">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="eb9d2-387">IntranetZoneAllowAccessToDataSources</span><span class="sxs-lookup"><span data-stu-id="eb9d2-387">IntranetZoneAllowAccessToDataSources</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-intranetzoneallowaccesstodatasources)
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb9d2-388">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="eb9d2-388">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="eb9d2-389">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="eb9d2-389">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="eb9d2-390">IntranetZoneAllowAutomaticPromptingForActiveXControls</span><span class="sxs-lookup"><span data-stu-id="eb9d2-390">IntranetZoneAllowAutomaticPromptingForActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-intranetzoneallowautomaticpromptingforactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb9d2-391">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="eb9d2-391">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="eb9d2-392">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="eb9d2-392">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="eb9d2-393">IntranetZoneAllowAutomaticPromptingForFileDownloads</span><span class="sxs-lookup"><span data-stu-id="eb9d2-393">IntranetZoneAllowAutomaticPromptingForFileDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-intranetzoneallowautomaticpromptingforfiledownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb9d2-394">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="eb9d2-394">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="eb9d2-395">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="eb9d2-395">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="eb9d2-396">IntranetZoneAllowFontDownloads</span><span class="sxs-lookup"><span data-stu-id="eb9d2-396">IntranetZoneAllowFontDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-intranetzoneallowfontdownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb9d2-397">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="eb9d2-397">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="eb9d2-398">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="eb9d2-398">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="eb9d2-399">IntranetZoneAllowLessPrivilegedSites</span><span class="sxs-lookup"><span data-stu-id="eb9d2-399">IntranetZoneAllowLessPrivilegedSites</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-intranetzoneallowlessprivilegedsites)
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb9d2-400">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="eb9d2-400">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="eb9d2-401">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="eb9d2-401">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="eb9d2-402">IntranetZoneAllowNETFrameworkReliantComponents</span><span class="sxs-lookup"><span data-stu-id="eb9d2-402">IntranetZoneAllowNETFrameworkReliantComponents</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-intranetzoneallownetframeworkreliantcomponents)
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb9d2-403">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="eb9d2-403">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="eb9d2-404">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="eb9d2-404">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="eb9d2-405">IntranetZoneAllowScriptlets</span><span class="sxs-lookup"><span data-stu-id="eb9d2-405">IntranetZoneAllowScriptlets</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-intranetzoneallowscriptlets)
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb9d2-406">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="eb9d2-406">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="eb9d2-407">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="eb9d2-407">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="eb9d2-408">IntranetZoneAllowSmartScreenIE</span><span class="sxs-lookup"><span data-stu-id="eb9d2-408">IntranetZoneAllowSmartScreenIE</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-intranetzoneallowsmartscreenie)
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb9d2-409">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="eb9d2-409">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="eb9d2-410">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="eb9d2-410">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="eb9d2-411">IntranetZoneAllowUserDataPersistence</span><span class="sxs-lookup"><span data-stu-id="eb9d2-411">IntranetZoneAllowUserDataPersistence</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-intranetzoneallowuserdatapersistence)
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb9d2-412">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="eb9d2-412">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="eb9d2-413">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="eb9d2-413">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="eb9d2-414">IntranetZoneDoNotRunAntimalwareAgainstActiveXControls</span><span class="sxs-lookup"><span data-stu-id="eb9d2-414">IntranetZoneDoNotRunAntimalwareAgainstActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-intranetzonedonotrunantimalwareagainstactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb9d2-415">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="eb9d2-415">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="eb9d2-416">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="eb9d2-416">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="eb9d2-417">IntranetZoneInitializeAndScriptActiveXControls</span><span class="sxs-lookup"><span data-stu-id="eb9d2-417">IntranetZoneInitializeAndScriptActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-intranetzoneinitializeandscriptactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb9d2-418">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="eb9d2-418">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="eb9d2-419">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="eb9d2-419">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="eb9d2-420">IntranetZoneInitializeAndScriptActiveXControlsNotMarkedSafe</span><span class="sxs-lookup"><span data-stu-id="eb9d2-420">IntranetZoneInitializeAndScriptActiveXControlsNotMarkedSafe</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb9d2-421">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="eb9d2-421">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="eb9d2-422">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="eb9d2-422">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="eb9d2-423">IntranetZoneJavaPermissions</span><span class="sxs-lookup"><span data-stu-id="eb9d2-423">IntranetZoneJavaPermissions</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-intranetzonejavapermissions)
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb9d2-424">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="eb9d2-424">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="eb9d2-425">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="eb9d2-425">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="eb9d2-426">IntranetZoneNavigateWindowsAndFrames</span><span class="sxs-lookup"><span data-stu-id="eb9d2-426">IntranetZoneNavigateWindowsAndFrames</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-intranetzonenavigatewindowsandframes)
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb9d2-427">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="eb9d2-427">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="eb9d2-428">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="eb9d2-428">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="eb9d2-429">LocalMachineZoneAllowAccessToDataSources</span><span class="sxs-lookup"><span data-stu-id="eb9d2-429">LocalMachineZoneAllowAccessToDataSources</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-localmachinezoneallowaccesstodatasources)
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb9d2-430">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="eb9d2-430">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="eb9d2-431">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="eb9d2-431">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="eb9d2-432">LocalMachineZoneAllowAutomaticPromptingForActiveXControls</span><span class="sxs-lookup"><span data-stu-id="eb9d2-432">LocalMachineZoneAllowAutomaticPromptingForActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-localmachinezoneallowautomaticpromptingforactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb9d2-433">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="eb9d2-433">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="eb9d2-434">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="eb9d2-434">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="eb9d2-435">LocalMachineZoneAllowAutomaticPromptingForFileDownloads</span><span class="sxs-lookup"><span data-stu-id="eb9d2-435">LocalMachineZoneAllowAutomaticPromptingForFileDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-localmachinezoneallowautomaticpromptingforfiledownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb9d2-436">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="eb9d2-436">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="eb9d2-437">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="eb9d2-437">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="eb9d2-438">LocalMachineZoneAllowFontDownloads</span><span class="sxs-lookup"><span data-stu-id="eb9d2-438">LocalMachineZoneAllowFontDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-localmachinezoneallowfontdownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb9d2-439">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="eb9d2-439">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="eb9d2-440">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="eb9d2-440">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="eb9d2-441">LocalMachineZoneAllowLessPrivilegedSites</span><span class="sxs-lookup"><span data-stu-id="eb9d2-441">LocalMachineZoneAllowLessPrivilegedSites</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-localmachinezoneallowlessprivilegedsites)
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb9d2-442">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="eb9d2-442">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="eb9d2-443">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="eb9d2-443">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="eb9d2-444">LocalMachineZoneAllowNETFrameworkReliantComponents</span><span class="sxs-lookup"><span data-stu-id="eb9d2-444">LocalMachineZoneAllowNETFrameworkReliantComponents</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-localmachinezoneallownetframeworkreliantcomponents)
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb9d2-445">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="eb9d2-445">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="eb9d2-446">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="eb9d2-446">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="eb9d2-447">LocalMachineZoneAllowScriptlets</span><span class="sxs-lookup"><span data-stu-id="eb9d2-447">LocalMachineZoneAllowScriptlets</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-localmachinezoneallowscriptlets)
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb9d2-448">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="eb9d2-448">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="eb9d2-449">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="eb9d2-449">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="eb9d2-450">LocalMachineZoneAllowSmartScreenIE</span><span class="sxs-lookup"><span data-stu-id="eb9d2-450">LocalMachineZoneAllowSmartScreenIE</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-localmachinezoneallowsmartscreenie)
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb9d2-451">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="eb9d2-451">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="eb9d2-452">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="eb9d2-452">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="eb9d2-453">LocalMachineZoneAllowUserDataPersistence</span><span class="sxs-lookup"><span data-stu-id="eb9d2-453">LocalMachineZoneAllowUserDataPersistence</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-localmachinezoneallowuserdatapersistence)
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb9d2-454">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="eb9d2-454">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="eb9d2-455">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="eb9d2-455">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="eb9d2-456">LocalMachineZoneDoNotRunAntimalwareAgainstActiveXControls</span><span class="sxs-lookup"><span data-stu-id="eb9d2-456">LocalMachineZoneDoNotRunAntimalwareAgainstActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-localmachinezonedonotrunantimalwareagainstactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb9d2-457">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="eb9d2-457">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="eb9d2-458">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="eb9d2-458">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="eb9d2-459">LocalMachineZoneInitializeAndScriptActiveXControls</span><span class="sxs-lookup"><span data-stu-id="eb9d2-459">LocalMachineZoneInitializeAndScriptActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-localmachinezoneinitializeandscriptactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb9d2-460">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="eb9d2-460">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="eb9d2-461">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="eb9d2-461">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="eb9d2-462">LocalMachineZoneJavaPermissions</span><span class="sxs-lookup"><span data-stu-id="eb9d2-462">LocalMachineZoneJavaPermissions</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-localmachinezonejavapermissions)
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb9d2-463">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="eb9d2-463">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="eb9d2-464">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="eb9d2-464">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="eb9d2-465">LocalMachineZoneNavigateWindowsAndFrames</span><span class="sxs-lookup"><span data-stu-id="eb9d2-465">LocalMachineZoneNavigateWindowsAndFrames</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-localmachinezonenavigatewindowsandframes)
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb9d2-466">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="eb9d2-466">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="eb9d2-467">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="eb9d2-467">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="eb9d2-468">LockedDownInternetZoneAllowAccessToDataSources</span><span class="sxs-lookup"><span data-stu-id="eb9d2-468">LockedDownInternetZoneAllowAccessToDataSources</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowninternetzoneallowaccesstodatasources)
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb9d2-469">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="eb9d2-469">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="eb9d2-470">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="eb9d2-470">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="eb9d2-471">LockedDownInternetZoneAllowAutomaticPromptingForActiveXControls</span><span class="sxs-lookup"><span data-stu-id="eb9d2-471">LockedDownInternetZoneAllowAutomaticPromptingForActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowninternetzoneallowautomaticpromptingforactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb9d2-472">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="eb9d2-472">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="eb9d2-473">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="eb9d2-473">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="eb9d2-474">LockedDownInternetZoneAllowAutomaticPromptingForFileDownloads</span><span class="sxs-lookup"><span data-stu-id="eb9d2-474">LockedDownInternetZoneAllowAutomaticPromptingForFileDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowninternetzoneallowautomaticpromptingforfiledownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb9d2-475">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="eb9d2-475">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="eb9d2-476">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="eb9d2-476">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="eb9d2-477">LockedDownInternetZoneAllowFontDownloads</span><span class="sxs-lookup"><span data-stu-id="eb9d2-477">LockedDownInternetZoneAllowFontDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowninternetzoneallowfontdownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb9d2-478">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="eb9d2-478">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="eb9d2-479">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="eb9d2-479">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="eb9d2-480">LockedDownInternetZoneAllowLessPrivilegedSites</span><span class="sxs-lookup"><span data-stu-id="eb9d2-480">LockedDownInternetZoneAllowLessPrivilegedSites</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowninternetzoneallowlessprivilegedsites)
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb9d2-481">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="eb9d2-481">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="eb9d2-482">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="eb9d2-482">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="eb9d2-483">LockedDownInternetZoneAllowNETFrameworkReliantComponents</span><span class="sxs-lookup"><span data-stu-id="eb9d2-483">LockedDownInternetZoneAllowNETFrameworkReliantComponents</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowninternetzoneallownetframeworkreliantcomponents)
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb9d2-484">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="eb9d2-484">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="eb9d2-485">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="eb9d2-485">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="eb9d2-486">LockedDownInternetZoneAllowScriptlets</span><span class="sxs-lookup"><span data-stu-id="eb9d2-486">LockedDownInternetZoneAllowScriptlets</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowninternetzoneallowscriptlets)
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb9d2-487">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="eb9d2-487">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="eb9d2-488">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="eb9d2-488">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="eb9d2-489">LockedDownInternetZoneAllowSmartScreenIE</span><span class="sxs-lookup"><span data-stu-id="eb9d2-489">LockedDownInternetZoneAllowSmartScreenIE</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowninternetzoneallowsmartscreenie)
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb9d2-490">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="eb9d2-490">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="eb9d2-491">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="eb9d2-491">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="eb9d2-492">LockedDownInternetZoneAllowUserDataPersistence</span><span class="sxs-lookup"><span data-stu-id="eb9d2-492">LockedDownInternetZoneAllowUserDataPersistence</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowninternetzoneallowuserdatapersistence)
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb9d2-493">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="eb9d2-493">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="eb9d2-494">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="eb9d2-494">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="eb9d2-495">LockedDownInternetZoneInitializeAndScriptActiveXControls</span><span class="sxs-lookup"><span data-stu-id="eb9d2-495">LockedDownInternetZoneInitializeAndScriptActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowninternetzoneinitializeandscriptactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb9d2-496">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="eb9d2-496">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="eb9d2-497">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="eb9d2-497">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="eb9d2-498">LockedDownInternetZoneJavaPermissions</span><span class="sxs-lookup"><span data-stu-id="eb9d2-498">LockedDownInternetZoneJavaPermissions</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowninternetzonejavapermissions)
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb9d2-499">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="eb9d2-499">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="eb9d2-500">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="eb9d2-500">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="eb9d2-501">LockedDownInternetZoneNavigateWindowsAndFrames</span><span class="sxs-lookup"><span data-stu-id="eb9d2-501">LockedDownInternetZoneNavigateWindowsAndFrames</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowninternetzonenavigatewindowsandframes)
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb9d2-502">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="eb9d2-502">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="eb9d2-503">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="eb9d2-503">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="eb9d2-504">LockedDownIntranetZoneAllowAccessToDataSources</span><span class="sxs-lookup"><span data-stu-id="eb9d2-504">LockedDownIntranetZoneAllowAccessToDataSources</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownintranetzoneallowaccesstodatasources)
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb9d2-505">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="eb9d2-505">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="eb9d2-506">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="eb9d2-506">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="eb9d2-507">LockedDownIntranetZoneAllowAutomaticPromptingForActiveXControls</span><span class="sxs-lookup"><span data-stu-id="eb9d2-507">LockedDownIntranetZoneAllowAutomaticPromptingForActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownintranetzoneallowautomaticpromptingforactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb9d2-508">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="eb9d2-508">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="eb9d2-509">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="eb9d2-509">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="eb9d2-510">LockedDownIntranetZoneAllowAutomaticPromptingForFileDownloads</span><span class="sxs-lookup"><span data-stu-id="eb9d2-510">LockedDownIntranetZoneAllowAutomaticPromptingForFileDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownintranetzoneallowautomaticpromptingforfiledownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb9d2-511">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="eb9d2-511">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="eb9d2-512">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="eb9d2-512">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="eb9d2-513">LockedDownIntranetZoneAllowFontDownloads</span><span class="sxs-lookup"><span data-stu-id="eb9d2-513">LockedDownIntranetZoneAllowFontDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownintranetzoneallowfontdownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb9d2-514">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="eb9d2-514">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="eb9d2-515">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="eb9d2-515">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="eb9d2-516">LockedDownIntranetZoneAllowLessPrivilegedSites</span><span class="sxs-lookup"><span data-stu-id="eb9d2-516">LockedDownIntranetZoneAllowLessPrivilegedSites</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownintranetzoneallowlessprivilegedsites)
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb9d2-517">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="eb9d2-517">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="eb9d2-518">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="eb9d2-518">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="eb9d2-519">LockedDownIntranetZoneAllowNETFrameworkReliantComponents</span><span class="sxs-lookup"><span data-stu-id="eb9d2-519">LockedDownIntranetZoneAllowNETFrameworkReliantComponents</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownintranetzoneallownetframeworkreliantcomponents)
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb9d2-520">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="eb9d2-520">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="eb9d2-521">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="eb9d2-521">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="eb9d2-522">LockedDownIntranetZoneAllowScriptlets</span><span class="sxs-lookup"><span data-stu-id="eb9d2-522">LockedDownIntranetZoneAllowScriptlets</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownintranetzoneallowscriptlets)
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb9d2-523">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="eb9d2-523">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="eb9d2-524">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="eb9d2-524">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="eb9d2-525">LockedDownIntranetZoneAllowSmartScreenIE</span><span class="sxs-lookup"><span data-stu-id="eb9d2-525">LockedDownIntranetZoneAllowSmartScreenIE</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownintranetzoneallowsmartscreenie)
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb9d2-526">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="eb9d2-526">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="eb9d2-527">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="eb9d2-527">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="eb9d2-528">LockedDownIntranetZoneAllowUserDataPersistence</span><span class="sxs-lookup"><span data-stu-id="eb9d2-528">LockedDownIntranetZoneAllowUserDataPersistence</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownintranetzoneallowuserdatapersistence)
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb9d2-529">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="eb9d2-529">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="eb9d2-530">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="eb9d2-530">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="eb9d2-531">LockedDownIntranetZoneInitializeAndScriptActiveXControls</span><span class="sxs-lookup"><span data-stu-id="eb9d2-531">LockedDownIntranetZoneInitializeAndScriptActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownintranetzoneinitializeandscriptactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb9d2-532">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="eb9d2-532">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="eb9d2-533">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="eb9d2-533">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="eb9d2-534">LockedDownIntranetZoneNavigateWindowsAndFrames</span><span class="sxs-lookup"><span data-stu-id="eb9d2-534">LockedDownIntranetZoneNavigateWindowsAndFrames</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownintranetzonenavigatewindowsandframes)
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb9d2-535">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="eb9d2-535">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="eb9d2-536">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="eb9d2-536">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="eb9d2-537">LockedDownLocalMachineZoneAllowAccessToDataSources</span><span class="sxs-lookup"><span data-stu-id="eb9d2-537">LockedDownLocalMachineZoneAllowAccessToDataSources</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownlocalmachinezoneallowaccesstodatasources)
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb9d2-538">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="eb9d2-538">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="eb9d2-539">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="eb9d2-539">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="eb9d2-540">LockedDownLocalMachineZoneAllowAutomaticPromptingForActiveXControls</span><span class="sxs-lookup"><span data-stu-id="eb9d2-540">LockedDownLocalMachineZoneAllowAutomaticPromptingForActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownlocalmachinezoneallowautomaticpromptingforactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb9d2-541">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="eb9d2-541">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="eb9d2-542">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="eb9d2-542">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="eb9d2-543">LockedDownLocalMachineZoneAllowAutomaticPromptingForFileDownloads</span><span class="sxs-lookup"><span data-stu-id="eb9d2-543">LockedDownLocalMachineZoneAllowAutomaticPromptingForFileDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownlocalmachinezoneallowautomaticpromptingforfiledownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb9d2-544">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="eb9d2-544">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="eb9d2-545">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="eb9d2-545">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="eb9d2-546">LockedDownLocalMachineZoneAllowFontDownloads</span><span class="sxs-lookup"><span data-stu-id="eb9d2-546">LockedDownLocalMachineZoneAllowFontDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownlocalmachinezoneallowfontdownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb9d2-547">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="eb9d2-547">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="eb9d2-548">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="eb9d2-548">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="eb9d2-549">LockedDownLocalMachineZoneAllowLessPrivilegedSites</span><span class="sxs-lookup"><span data-stu-id="eb9d2-549">LockedDownLocalMachineZoneAllowLessPrivilegedSites</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownlocalmachinezoneallowlessprivilegedsites)
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb9d2-550">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="eb9d2-550">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="eb9d2-551">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="eb9d2-551">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="eb9d2-552">LockedDownLocalMachineZoneAllowNETFrameworkReliantComponents</span><span class="sxs-lookup"><span data-stu-id="eb9d2-552">LockedDownLocalMachineZoneAllowNETFrameworkReliantComponents</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownlocalmachinezoneallownetframeworkreliantcomponents)
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb9d2-553">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="eb9d2-553">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="eb9d2-554">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="eb9d2-554">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="eb9d2-555">LockedDownLocalMachineZoneAllowScriptlets</span><span class="sxs-lookup"><span data-stu-id="eb9d2-555">LockedDownLocalMachineZoneAllowScriptlets</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownlocalmachinezoneallowscriptlets)
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb9d2-556">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="eb9d2-556">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="eb9d2-557">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="eb9d2-557">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="eb9d2-558">LockedDownLocalMachineZoneAllowSmartScreenIE</span><span class="sxs-lookup"><span data-stu-id="eb9d2-558">LockedDownLocalMachineZoneAllowSmartScreenIE</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownlocalmachinezoneallowsmartscreenie)
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb9d2-559">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="eb9d2-559">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="eb9d2-560">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="eb9d2-560">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="eb9d2-561">LockedDownLocalMachineZoneAllowUserDataPersistence</span><span class="sxs-lookup"><span data-stu-id="eb9d2-561">LockedDownLocalMachineZoneAllowUserDataPersistence</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownlocalmachinezoneallowuserdatapersistence)
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb9d2-562">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="eb9d2-562">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="eb9d2-563">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="eb9d2-563">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="eb9d2-564">LockedDownLocalMachineZoneInitializeAndScriptActiveXControls</span><span class="sxs-lookup"><span data-stu-id="eb9d2-564">LockedDownLocalMachineZoneInitializeAndScriptActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownlocalmachinezoneinitializeandscriptactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb9d2-565">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="eb9d2-565">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="eb9d2-566">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="eb9d2-566">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="eb9d2-567">LockedDownLocalMachineZoneJavaPermissions</span><span class="sxs-lookup"><span data-stu-id="eb9d2-567">LockedDownLocalMachineZoneJavaPermissions</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownlocalmachinezonejavapermissions)
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb9d2-568">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="eb9d2-568">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="eb9d2-569">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="eb9d2-569">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="eb9d2-570">LockedDownLocalMachineZoneNavigateWindowsAndFrames</span><span class="sxs-lookup"><span data-stu-id="eb9d2-570">LockedDownLocalMachineZoneNavigateWindowsAndFrames</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownlocalmachinezonenavigatewindowsandframes)
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb9d2-571">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="eb9d2-571">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="eb9d2-572">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="eb9d2-572">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="eb9d2-573">LockedDownRestrictedSitesZoneAllowAccessToDataSources</span><span class="sxs-lookup"><span data-stu-id="eb9d2-573">LockedDownRestrictedSitesZoneAllowAccessToDataSources</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownrestrictedsiteszoneallowaccesstodatasources)
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb9d2-574">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="eb9d2-574">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="eb9d2-575">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="eb9d2-575">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="eb9d2-576">LockedDownRestrictedSitesZoneAllowAutomaticPromptingForActiveXControls</span><span class="sxs-lookup"><span data-stu-id="eb9d2-576">LockedDownRestrictedSitesZoneAllowAutomaticPromptingForActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownrestrictedsiteszoneallowautomaticpromptingforactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb9d2-577">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="eb9d2-577">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="eb9d2-578">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="eb9d2-578">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="eb9d2-579">LockedDownRestrictedSitesZoneAllowAutomaticPromptingForFileDownloads</span><span class="sxs-lookup"><span data-stu-id="eb9d2-579">LockedDownRestrictedSitesZoneAllowAutomaticPromptingForFileDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownrestrictedsiteszoneallowautomaticpromptingforfiledownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb9d2-580">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="eb9d2-580">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="eb9d2-581">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="eb9d2-581">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="eb9d2-582">LockedDownRestrictedSitesZoneAllowFontDownloads</span><span class="sxs-lookup"><span data-stu-id="eb9d2-582">LockedDownRestrictedSitesZoneAllowFontDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownrestrictedsiteszoneallowfontdownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb9d2-583">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="eb9d2-583">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="eb9d2-584">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="eb9d2-584">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="eb9d2-585">LockedDownRestrictedSitesZoneAllowLessPrivilegedSites</span><span class="sxs-lookup"><span data-stu-id="eb9d2-585">LockedDownRestrictedSitesZoneAllowLessPrivilegedSites</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownrestrictedsiteszoneallowlessprivilegedsites)
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb9d2-586">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="eb9d2-586">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="eb9d2-587">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="eb9d2-587">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="eb9d2-588">LockedDownRestrictedSitesZoneAllowNETFrameworkReliantComponents</span><span class="sxs-lookup"><span data-stu-id="eb9d2-588">LockedDownRestrictedSitesZoneAllowNETFrameworkReliantComponents</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownrestrictedsiteszoneallownetframeworkreliantcomponents)
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb9d2-589">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="eb9d2-589">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="eb9d2-590">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="eb9d2-590">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="eb9d2-591">LockedDownRestrictedSitesZoneAllowScriptlets</span><span class="sxs-lookup"><span data-stu-id="eb9d2-591">LockedDownRestrictedSitesZoneAllowScriptlets</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownrestrictedsiteszoneallowscriptlets)
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb9d2-592">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="eb9d2-592">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="eb9d2-593">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="eb9d2-593">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="eb9d2-594">LockedDownRestrictedSitesZoneAllowSmartScreenIE</span><span class="sxs-lookup"><span data-stu-id="eb9d2-594">LockedDownRestrictedSitesZoneAllowSmartScreenIE</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownrestrictedsiteszoneallowsmartscreenie)
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb9d2-595">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="eb9d2-595">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="eb9d2-596">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="eb9d2-596">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="eb9d2-597">LockedDownRestrictedSitesZoneAllowUserDataPersistence</span><span class="sxs-lookup"><span data-stu-id="eb9d2-597">LockedDownRestrictedSitesZoneAllowUserDataPersistence</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownrestrictedsiteszoneallowuserdatapersistence)
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb9d2-598">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="eb9d2-598">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="eb9d2-599">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="eb9d2-599">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="eb9d2-600">LockedDownRestrictedSitesZoneInitializeAndScriptActiveXControls</span><span class="sxs-lookup"><span data-stu-id="eb9d2-600">LockedDownRestrictedSitesZoneInitializeAndScriptActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownrestrictedsiteszoneinitializeandscriptactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb9d2-601">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="eb9d2-601">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="eb9d2-602">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="eb9d2-602">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="eb9d2-603">LockedDownRestrictedSitesZoneJavaPermissions</span><span class="sxs-lookup"><span data-stu-id="eb9d2-603">LockedDownRestrictedSitesZoneJavaPermissions</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownrestrictedsiteszonejavapermissions)
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb9d2-604">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="eb9d2-604">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="eb9d2-605">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="eb9d2-605">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="eb9d2-606">LockedDownRestrictedSitesZoneNavigateWindowsAndFrames</span><span class="sxs-lookup"><span data-stu-id="eb9d2-606">LockedDownRestrictedSitesZoneNavigateWindowsAndFrames</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownrestrictedsiteszonenavigatewindowsandframes)
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb9d2-607">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="eb9d2-607">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="eb9d2-608">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="eb9d2-608">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="eb9d2-609">LockedDownTrustedSitesZoneAllowAccessToDataSources</span><span class="sxs-lookup"><span data-stu-id="eb9d2-609">LockedDownTrustedSitesZoneAllowAccessToDataSources</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowntrustedsiteszoneallowaccesstodatasources)
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb9d2-610">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="eb9d2-610">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="eb9d2-611">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="eb9d2-611">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="eb9d2-612">LockedDownTrustedSitesZoneAllowAutomaticPromptingForActiveXControls</span><span class="sxs-lookup"><span data-stu-id="eb9d2-612">LockedDownTrustedSitesZoneAllowAutomaticPromptingForActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowntrustedsiteszoneallowautomaticpromptingforactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb9d2-613">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="eb9d2-613">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="eb9d2-614">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="eb9d2-614">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="eb9d2-615">LockedDownTrustedSitesZoneAllowAutomaticPromptingForFileDownloads</span><span class="sxs-lookup"><span data-stu-id="eb9d2-615">LockedDownTrustedSitesZoneAllowAutomaticPromptingForFileDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowntrustedsiteszoneallowautomaticpromptingforfiledownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb9d2-616">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="eb9d2-616">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="eb9d2-617">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="eb9d2-617">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="eb9d2-618">LockedDownTrustedSitesZoneAllowFontDownloads</span><span class="sxs-lookup"><span data-stu-id="eb9d2-618">LockedDownTrustedSitesZoneAllowFontDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowntrustedsiteszoneallowfontdownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb9d2-619">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="eb9d2-619">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="eb9d2-620">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="eb9d2-620">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="eb9d2-621">LockedDownTrustedSitesZoneAllowLessPrivilegedSites</span><span class="sxs-lookup"><span data-stu-id="eb9d2-621">LockedDownTrustedSitesZoneAllowLessPrivilegedSites</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowntrustedsiteszoneallowlessprivilegedsites)
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb9d2-622">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="eb9d2-622">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="eb9d2-623">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="eb9d2-623">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="eb9d2-624">LockedDownTrustedSitesZoneAllowNETFrameworkReliantComponents</span><span class="sxs-lookup"><span data-stu-id="eb9d2-624">LockedDownTrustedSitesZoneAllowNETFrameworkReliantComponents</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowntrustedsiteszoneallownetframeworkreliantcomponents)
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb9d2-625">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="eb9d2-625">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="eb9d2-626">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="eb9d2-626">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="eb9d2-627">LockedDownTrustedSitesZoneAllowScriptlets</span><span class="sxs-lookup"><span data-stu-id="eb9d2-627">LockedDownTrustedSitesZoneAllowScriptlets</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowntrustedsiteszoneallowscriptlets)
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb9d2-628">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="eb9d2-628">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="eb9d2-629">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="eb9d2-629">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="eb9d2-630">LockedDownTrustedSitesZoneAllowSmartScreenIE</span><span class="sxs-lookup"><span data-stu-id="eb9d2-630">LockedDownTrustedSitesZoneAllowSmartScreenIE</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowntrustedsiteszoneallowsmartscreenie)
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb9d2-631">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="eb9d2-631">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="eb9d2-632">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="eb9d2-632">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="eb9d2-633">LockedDownTrustedSitesZoneAllowUserDataPersistence</span><span class="sxs-lookup"><span data-stu-id="eb9d2-633">LockedDownTrustedSitesZoneAllowUserDataPersistence</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowntrustedsiteszoneallowuserdatapersistence)
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb9d2-634">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="eb9d2-634">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="eb9d2-635">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="eb9d2-635">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="eb9d2-636">LockedDownTrustedSitesZoneInitializeAndScriptActiveXControls</span><span class="sxs-lookup"><span data-stu-id="eb9d2-636">LockedDownTrustedSitesZoneInitializeAndScriptActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowntrustedsiteszoneinitializeandscriptactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb9d2-637">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="eb9d2-637">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="eb9d2-638">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="eb9d2-638">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="eb9d2-639">LockedDownTrustedSitesZoneJavaPermissions</span><span class="sxs-lookup"><span data-stu-id="eb9d2-639">LockedDownTrustedSitesZoneJavaPermissions</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowntrustedsiteszonejavapermissions)
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb9d2-640">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="eb9d2-640">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="eb9d2-641">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="eb9d2-641">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="eb9d2-642">LockedDownTrustedSitesZoneNavigateWindowsAndFrames</span><span class="sxs-lookup"><span data-stu-id="eb9d2-642">LockedDownTrustedSitesZoneNavigateWindowsAndFrames</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowntrustedsiteszonenavigatewindowsandframes)
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb9d2-643">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="eb9d2-643">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="eb9d2-644">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="eb9d2-644">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="eb9d2-645">MimeSniffingSafetyFeatureInternetExplorerProcesses</span><span class="sxs-lookup"><span data-stu-id="eb9d2-645">MimeSniffingSafetyFeatureInternetExplorerProcesses</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-mimesniffingsafetyfeatureinternetexplorerprocesses)
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb9d2-646">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="eb9d2-646">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="eb9d2-647">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="eb9d2-647">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="eb9d2-648">MKProtocolSecurityRestrictionInternetExplorerProcesses</span><span class="sxs-lookup"><span data-stu-id="eb9d2-648">MKProtocolSecurityRestrictionInternetExplorerProcesses</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-mkprotocolsecurityrestrictioninternetexplorerprocesses)
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb9d2-649">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="eb9d2-649">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="eb9d2-650">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="eb9d2-650">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="eb9d2-651">NotificationBarInternetExplorerProcesses</span><span class="sxs-lookup"><span data-stu-id="eb9d2-651">NotificationBarInternetExplorerProcesses</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-notificationbarinternetexplorerprocesses)
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb9d2-652">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="eb9d2-652">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="eb9d2-653">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="eb9d2-653">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="eb9d2-654">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="eb9d2-654">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb9d2-655">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="eb9d2-655">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="eb9d2-656">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="eb9d2-656">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="eb9d2-657">Calificadores: [ **clave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="eb9d2-657">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="eb9d2-658">PreventManagingSmartScreenFilter</span><span class="sxs-lookup"><span data-stu-id="eb9d2-658">PreventManagingSmartScreenFilter</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-preventmanagingsmartscreenfilter)
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb9d2-659">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="eb9d2-659">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="eb9d2-660">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="eb9d2-660">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="eb9d2-661">PreventPerUserInstallationOfActiveXControls</span><span class="sxs-lookup"><span data-stu-id="eb9d2-661">PreventPerUserInstallationOfActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-preventperuserinstallationofactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb9d2-662">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="eb9d2-662">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="eb9d2-663">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="eb9d2-663">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="eb9d2-664">ProtectionFromZoneElevationInternetExplorerProcesses</span><span class="sxs-lookup"><span data-stu-id="eb9d2-664">ProtectionFromZoneElevationInternetExplorerProcesses</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-protectionfromzoneelevationinternetexplorerprocesses)
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb9d2-665">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="eb9d2-665">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="eb9d2-666">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="eb9d2-666">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="eb9d2-667">RemoveRunThisTimeButtonForOutdatedActiveXControls</span><span class="sxs-lookup"><span data-stu-id="eb9d2-667">RemoveRunThisTimeButtonForOutdatedActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-removerunthistimebuttonforoutdatedactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb9d2-668">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="eb9d2-668">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="eb9d2-669">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="eb9d2-669">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="eb9d2-670">RestrictActiveXInstallInternetExplorerProcesses</span><span class="sxs-lookup"><span data-stu-id="eb9d2-670">RestrictActiveXInstallInternetExplorerProcesses</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictactivexinstallinternetexplorerprocesses)
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb9d2-671">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="eb9d2-671">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="eb9d2-672">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="eb9d2-672">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="eb9d2-673">RestrictedSitesZoneAllowAccessToDataSources</span><span class="sxs-lookup"><span data-stu-id="eb9d2-673">RestrictedSitesZoneAllowAccessToDataSources</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallowaccesstodatasources)
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb9d2-674">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="eb9d2-674">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="eb9d2-675">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="eb9d2-675">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="eb9d2-676">RestrictedSitesZoneAllowActiveScripting</span><span class="sxs-lookup"><span data-stu-id="eb9d2-676">RestrictedSitesZoneAllowActiveScripting</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallowactivescripting)
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb9d2-677">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="eb9d2-677">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="eb9d2-678">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="eb9d2-678">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="eb9d2-679">RestrictedSitesZoneAllowAutomaticPromptingForActiveXControls</span><span class="sxs-lookup"><span data-stu-id="eb9d2-679">RestrictedSitesZoneAllowAutomaticPromptingForActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallowautomaticpromptingforactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb9d2-680">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="eb9d2-680">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="eb9d2-681">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="eb9d2-681">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="eb9d2-682">RestrictedSitesZoneAllowAutomaticPromptingForFileDownloads</span><span class="sxs-lookup"><span data-stu-id="eb9d2-682">RestrictedSitesZoneAllowAutomaticPromptingForFileDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallowautomaticpromptingforfiledownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb9d2-683">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="eb9d2-683">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="eb9d2-684">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="eb9d2-684">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="eb9d2-685">RestrictedSitesZoneAllowBinaryAndScriptBehaviors</span><span class="sxs-lookup"><span data-stu-id="eb9d2-685">RestrictedSitesZoneAllowBinaryAndScriptBehaviors</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallowbinaryandscriptbehaviors)
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb9d2-686">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="eb9d2-686">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="eb9d2-687">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="eb9d2-687">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="eb9d2-688">RestrictedSitesZoneAllowCopyPasteViaScript</span><span class="sxs-lookup"><span data-stu-id="eb9d2-688">RestrictedSitesZoneAllowCopyPasteViaScript</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallowcopypasteviascript)
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb9d2-689">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="eb9d2-689">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="eb9d2-690">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="eb9d2-690">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="eb9d2-691">RestrictedSitesZoneAllowDragAndDropCopyAndPasteFiles</span><span class="sxs-lookup"><span data-stu-id="eb9d2-691">RestrictedSitesZoneAllowDragAndDropCopyAndPasteFiles</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallowdraganddropcopyandpastefiles)
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb9d2-692">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="eb9d2-692">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="eb9d2-693">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="eb9d2-693">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="eb9d2-694">RestrictedSitesZoneAllowFileDownloads</span><span class="sxs-lookup"><span data-stu-id="eb9d2-694">RestrictedSitesZoneAllowFileDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallowfiledownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb9d2-695">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="eb9d2-695">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="eb9d2-696">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="eb9d2-696">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="eb9d2-697">RestrictedSitesZoneAllowFontDownloads</span><span class="sxs-lookup"><span data-stu-id="eb9d2-697">RestrictedSitesZoneAllowFontDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallowfontdownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb9d2-698">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="eb9d2-698">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="eb9d2-699">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="eb9d2-699">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="eb9d2-700">RestrictedSitesZoneAllowLessPrivilegedSites</span><span class="sxs-lookup"><span data-stu-id="eb9d2-700">RestrictedSitesZoneAllowLessPrivilegedSites</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallowlessprivilegedsites)
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb9d2-701">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="eb9d2-701">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="eb9d2-702">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="eb9d2-702">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="eb9d2-703">RestrictedSitesZoneAllowLoadingOfXAMLFiles</span><span class="sxs-lookup"><span data-stu-id="eb9d2-703">RestrictedSitesZoneAllowLoadingOfXAMLFiles</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallowloadingofxamlfiles)
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb9d2-704">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="eb9d2-704">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="eb9d2-705">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="eb9d2-705">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="eb9d2-706">RestrictedSitesZoneAllowMETAREFRESH</span><span class="sxs-lookup"><span data-stu-id="eb9d2-706">RestrictedSitesZoneAllowMETAREFRESH</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallowmetarefresh)
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb9d2-707">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="eb9d2-707">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="eb9d2-708">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="eb9d2-708">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="eb9d2-709">RestrictedSitesZoneAllowNETFrameworkReliantComponents</span><span class="sxs-lookup"><span data-stu-id="eb9d2-709">RestrictedSitesZoneAllowNETFrameworkReliantComponents</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallownetframeworkreliantcomponents)
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb9d2-710">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="eb9d2-710">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="eb9d2-711">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="eb9d2-711">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="eb9d2-712">RestrictedSitesZoneAllowOnlyApprovedDomainsToUseActiveXControls</span><span class="sxs-lookup"><span data-stu-id="eb9d2-712">RestrictedSitesZoneAllowOnlyApprovedDomainsToUseActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallowonlyapproveddomainstouseactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb9d2-713">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="eb9d2-713">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="eb9d2-714">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="eb9d2-714">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="eb9d2-715">RestrictedSitesZoneAllowOnlyApprovedDomainsToUseTDCActiveXControl</span><span class="sxs-lookup"><span data-stu-id="eb9d2-715">RestrictedSitesZoneAllowOnlyApprovedDomainsToUseTDCActiveXControl</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallowonlyapproveddomainstousetdcactivexcontrol)
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb9d2-716">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="eb9d2-716">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="eb9d2-717">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="eb9d2-717">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="eb9d2-718">RestrictedSitesZoneAllowScriptingOfInternetExplorerWebBrowserControls</span><span class="sxs-lookup"><span data-stu-id="eb9d2-718">RestrictedSitesZoneAllowScriptingOfInternetExplorerWebBrowserControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallowscriptingofinternetexplorerwebbrowsercontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb9d2-719">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="eb9d2-719">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="eb9d2-720">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="eb9d2-720">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="eb9d2-721">RestrictedSitesZoneAllowScriptInitiatedWindows</span><span class="sxs-lookup"><span data-stu-id="eb9d2-721">RestrictedSitesZoneAllowScriptInitiatedWindows</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallowscriptinitiatedwindows)
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb9d2-722">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="eb9d2-722">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="eb9d2-723">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="eb9d2-723">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="eb9d2-724">RestrictedSitesZoneAllowScriptlets</span><span class="sxs-lookup"><span data-stu-id="eb9d2-724">RestrictedSitesZoneAllowScriptlets</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallowscriptlets)
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb9d2-725">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="eb9d2-725">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="eb9d2-726">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="eb9d2-726">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="eb9d2-727">RestrictedSitesZoneAllowSmartScreenIE</span><span class="sxs-lookup"><span data-stu-id="eb9d2-727">RestrictedSitesZoneAllowSmartScreenIE</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallowsmartscreenie)
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb9d2-728">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="eb9d2-728">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="eb9d2-729">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="eb9d2-729">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="eb9d2-730">RestrictedSitesZoneAllowUpdatesToStatusBarViaScript</span><span class="sxs-lookup"><span data-stu-id="eb9d2-730">RestrictedSitesZoneAllowUpdatesToStatusBarViaScript</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallowupdatestostatusbarviascript)
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb9d2-731">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="eb9d2-731">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="eb9d2-732">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="eb9d2-732">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="eb9d2-733">RestrictedSitesZoneAllowUserDataPersistence</span><span class="sxs-lookup"><span data-stu-id="eb9d2-733">RestrictedSitesZoneAllowUserDataPersistence</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallowuserdatapersistence)
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb9d2-734">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="eb9d2-734">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="eb9d2-735">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="eb9d2-735">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="eb9d2-736">RestrictedSitesZoneDoNotRunAntimalwareAgainstActiveXControls</span><span class="sxs-lookup"><span data-stu-id="eb9d2-736">RestrictedSitesZoneDoNotRunAntimalwareAgainstActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszonedonotrunantimalwareagainstactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb9d2-737">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="eb9d2-737">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="eb9d2-738">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="eb9d2-738">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="eb9d2-739">RestrictedSitesZoneDownloadSignedActiveXControls</span><span class="sxs-lookup"><span data-stu-id="eb9d2-739">RestrictedSitesZoneDownloadSignedActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszonedownloadsignedactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb9d2-740">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="eb9d2-740">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="eb9d2-741">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="eb9d2-741">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="eb9d2-742">RestrictedSitesZoneDownloadUnsignedActiveXControls</span><span class="sxs-lookup"><span data-stu-id="eb9d2-742">RestrictedSitesZoneDownloadUnsignedActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszonedownloadunsignedactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb9d2-743">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="eb9d2-743">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="eb9d2-744">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="eb9d2-744">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="eb9d2-745">RestrictedSitesZoneEnableCrossSiteScriptingFilter</span><span class="sxs-lookup"><span data-stu-id="eb9d2-745">RestrictedSitesZoneEnableCrossSiteScriptingFilter</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneenablecrosssitescriptingfilter)
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb9d2-746">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="eb9d2-746">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="eb9d2-747">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="eb9d2-747">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="eb9d2-748">RestrictedSitesZoneEnableDraggingOfContentFromDifferentDomainsAcrossWindows</span><span class="sxs-lookup"><span data-stu-id="eb9d2-748">RestrictedSitesZoneEnableDraggingOfContentFromDifferentDomainsAcrossWindows</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneenabledraggingofcontentfromdifferentdomainsacrosswindows)
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb9d2-749">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="eb9d2-749">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="eb9d2-750">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="eb9d2-750">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="eb9d2-751">RestrictedSitesZoneEnableDraggingOfContentFromDifferentDomainsWithinWindows</span><span class="sxs-lookup"><span data-stu-id="eb9d2-751">RestrictedSitesZoneEnableDraggingOfContentFromDifferentDomainsWithinWindows</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneenabledraggingofcontentfromdifferentdomainswithinwindows)
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb9d2-752">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="eb9d2-752">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="eb9d2-753">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="eb9d2-753">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="eb9d2-754">RestrictedSitesZoneEnableMIMESniffing</span><span class="sxs-lookup"><span data-stu-id="eb9d2-754">RestrictedSitesZoneEnableMIMESniffing</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneenablemimesniffing)
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb9d2-755">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="eb9d2-755">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="eb9d2-756">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="eb9d2-756">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="eb9d2-757">RestrictedSitesZoneIncludeLocalPathWhenUploadingFilesToServer</span><span class="sxs-lookup"><span data-stu-id="eb9d2-757">RestrictedSitesZoneIncludeLocalPathWhenUploadingFilesToServer</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneincludelocalpathwhenuploadingfilestoserver)
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb9d2-758">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="eb9d2-758">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="eb9d2-759">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="eb9d2-759">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="eb9d2-760">RestrictedSitesZoneInitializeAndScriptActiveXControls</span><span class="sxs-lookup"><span data-stu-id="eb9d2-760">RestrictedSitesZoneInitializeAndScriptActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneinitializeandscriptactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb9d2-761">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="eb9d2-761">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="eb9d2-762">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="eb9d2-762">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="eb9d2-763">RestrictedSitesZoneJavaPermissions</span><span class="sxs-lookup"><span data-stu-id="eb9d2-763">RestrictedSitesZoneJavaPermissions</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszonejavapermissions)
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb9d2-764">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="eb9d2-764">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="eb9d2-765">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="eb9d2-765">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="eb9d2-766">RestrictedSitesZoneLaunchingApplicationsAndFilesInIFRAME</span><span class="sxs-lookup"><span data-stu-id="eb9d2-766">RestrictedSitesZoneLaunchingApplicationsAndFilesInIFRAME</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszonelaunchingapplicationsandfilesiniframe)
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb9d2-767">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="eb9d2-767">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="eb9d2-768">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="eb9d2-768">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="eb9d2-769">RestrictedSitesZoneLogonOptions</span><span class="sxs-lookup"><span data-stu-id="eb9d2-769">RestrictedSitesZoneLogonOptions</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszonelogonoptions)
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb9d2-770">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="eb9d2-770">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="eb9d2-771">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="eb9d2-771">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="eb9d2-772">RestrictedSitesZoneNavigateWindowsAndFrames</span><span class="sxs-lookup"><span data-stu-id="eb9d2-772">RestrictedSitesZoneNavigateWindowsAndFrames</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszonenavigatewindowsandframes)
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb9d2-773">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="eb9d2-773">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="eb9d2-774">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="eb9d2-774">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="eb9d2-775">RestrictedSitesZoneNavigateWindowsAndFramesAcrossDomains</span><span class="sxs-lookup"><span data-stu-id="eb9d2-775">RestrictedSitesZoneNavigateWindowsAndFramesAcrossDomains</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb9d2-776">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="eb9d2-776">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="eb9d2-777">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="eb9d2-777">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="eb9d2-778">RestrictedSitesZoneRunActiveXControlsAndPlugins</span><span class="sxs-lookup"><span data-stu-id="eb9d2-778">RestrictedSitesZoneRunActiveXControlsAndPlugins</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszonerunactivexcontrolsandplugins)
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb9d2-779">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="eb9d2-779">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="eb9d2-780">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="eb9d2-780">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="eb9d2-781">RestrictedSitesZoneRunNETFrameworkReliantComponentsSignedWithAuthenticode</span><span class="sxs-lookup"><span data-stu-id="eb9d2-781">RestrictedSitesZoneRunNETFrameworkReliantComponentsSignedWithAuthenticode</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszonerunnetframeworkreliantcomponentssignedwithauthenticode)
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb9d2-782">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="eb9d2-782">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="eb9d2-783">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="eb9d2-783">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="eb9d2-784">RestrictedSitesZoneScriptActiveXControlsMarkedSafeForScripting</span><span class="sxs-lookup"><span data-stu-id="eb9d2-784">RestrictedSitesZoneScriptActiveXControlsMarkedSafeForScripting</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszonescriptactivexcontrolsmarkedsafeforscripting)
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb9d2-785">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="eb9d2-785">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="eb9d2-786">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="eb9d2-786">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="eb9d2-787">RestrictedSitesZoneScriptingOfJavaApplets</span><span class="sxs-lookup"><span data-stu-id="eb9d2-787">RestrictedSitesZoneScriptingOfJavaApplets</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszonescriptingofjavaapplets)
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb9d2-788">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="eb9d2-788">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="eb9d2-789">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="eb9d2-789">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="eb9d2-790">RestrictedSitesZoneShowSecurityWarningForPotentiallyUnsafeFiles</span><span class="sxs-lookup"><span data-stu-id="eb9d2-790">RestrictedSitesZoneShowSecurityWarningForPotentiallyUnsafeFiles</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneshowsecuritywarningforpotentiallyunsafefiles)
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb9d2-791">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="eb9d2-791">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="eb9d2-792">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="eb9d2-792">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="eb9d2-793">RestrictedSitesZoneTurnOnCrossSiteScriptingFilter</span><span class="sxs-lookup"><span data-stu-id="eb9d2-793">RestrictedSitesZoneTurnOnCrossSiteScriptingFilter</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb9d2-794">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="eb9d2-794">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="eb9d2-795">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="eb9d2-795">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="eb9d2-796">RestrictedSitesZoneTurnOnProtectedMode</span><span class="sxs-lookup"><span data-stu-id="eb9d2-796">RestrictedSitesZoneTurnOnProtectedMode</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneturnonprotectedmode)
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb9d2-797">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="eb9d2-797">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="eb9d2-798">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="eb9d2-798">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="eb9d2-799">RestrictedSitesZoneUsePopupBlocker</span><span class="sxs-lookup"><span data-stu-id="eb9d2-799">RestrictedSitesZoneUsePopupBlocker</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneusepopupblocker)
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb9d2-800">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="eb9d2-800">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="eb9d2-801">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="eb9d2-801">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="eb9d2-802">RestrictFileDownloadInternetExplorerProcesses</span><span class="sxs-lookup"><span data-stu-id="eb9d2-802">RestrictFileDownloadInternetExplorerProcesses</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictfiledownloadinternetexplorerprocesses)
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb9d2-803">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="eb9d2-803">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="eb9d2-804">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="eb9d2-804">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="eb9d2-805">ScriptedWindowSecurityRestrictionsInternetExplorerProcesses</span><span class="sxs-lookup"><span data-stu-id="eb9d2-805">ScriptedWindowSecurityRestrictionsInternetExplorerProcesses</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-scriptedwindowsecurityrestrictionsinternetexplorerprocesses)
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb9d2-806">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="eb9d2-806">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="eb9d2-807">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="eb9d2-807">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="eb9d2-808">SearchProviderList</span><span class="sxs-lookup"><span data-stu-id="eb9d2-808">SearchProviderList</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-searchproviderlist)
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb9d2-809">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="eb9d2-809">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="eb9d2-810">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="eb9d2-810">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="eb9d2-811">SpecifyUseOfActiveXInstallerService</span><span class="sxs-lookup"><span data-stu-id="eb9d2-811">SpecifyUseOfActiveXInstallerService</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-specifyuseofactivexinstallerservice)
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb9d2-812">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="eb9d2-812">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="eb9d2-813">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="eb9d2-813">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="eb9d2-814">TrustedSitesZoneAllowAccessToDataSources</span><span class="sxs-lookup"><span data-stu-id="eb9d2-814">TrustedSitesZoneAllowAccessToDataSources</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-trustedsiteszoneallowaccesstodatasources)
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb9d2-815">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="eb9d2-815">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="eb9d2-816">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="eb9d2-816">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="eb9d2-817">TrustedSitesZoneAllowAutomaticPromptingForActiveXControls</span><span class="sxs-lookup"><span data-stu-id="eb9d2-817">TrustedSitesZoneAllowAutomaticPromptingForActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-trustedsiteszoneallowautomaticpromptingforactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb9d2-818">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="eb9d2-818">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="eb9d2-819">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="eb9d2-819">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="eb9d2-820">TrustedSitesZoneAllowAutomaticPromptingForFileDownloads</span><span class="sxs-lookup"><span data-stu-id="eb9d2-820">TrustedSitesZoneAllowAutomaticPromptingForFileDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-trustedsiteszoneallowautomaticpromptingforfiledownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb9d2-821">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="eb9d2-821">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="eb9d2-822">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="eb9d2-822">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="eb9d2-823">TrustedSitesZoneAllowFontDownloads</span><span class="sxs-lookup"><span data-stu-id="eb9d2-823">TrustedSitesZoneAllowFontDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-trustedsiteszoneallowfontdownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb9d2-824">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="eb9d2-824">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="eb9d2-825">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="eb9d2-825">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="eb9d2-826">TrustedSitesZoneAllowLessPrivilegedSites</span><span class="sxs-lookup"><span data-stu-id="eb9d2-826">TrustedSitesZoneAllowLessPrivilegedSites</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-trustedsiteszoneallowlessprivilegedsites)
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb9d2-827">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="eb9d2-827">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="eb9d2-828">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="eb9d2-828">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="eb9d2-829">TrustedSitesZoneAllowNETFrameworkReliantComponents</span><span class="sxs-lookup"><span data-stu-id="eb9d2-829">TrustedSitesZoneAllowNETFrameworkReliantComponents</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-trustedsiteszoneallownetframeworkreliantcomponents)
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb9d2-830">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="eb9d2-830">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="eb9d2-831">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="eb9d2-831">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="eb9d2-832">TrustedSitesZoneAllowScriptlets</span><span class="sxs-lookup"><span data-stu-id="eb9d2-832">TrustedSitesZoneAllowScriptlets</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-trustedsiteszoneallowscriptlets)
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb9d2-833">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="eb9d2-833">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="eb9d2-834">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="eb9d2-834">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="eb9d2-835">TrustedSitesZoneAllowSmartScreenIE</span><span class="sxs-lookup"><span data-stu-id="eb9d2-835">TrustedSitesZoneAllowSmartScreenIE</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-trustedsiteszoneallowsmartscreenie)
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb9d2-836">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="eb9d2-836">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="eb9d2-837">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="eb9d2-837">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="eb9d2-838">TrustedSitesZoneAllowUserDataPersistence</span><span class="sxs-lookup"><span data-stu-id="eb9d2-838">TrustedSitesZoneAllowUserDataPersistence</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-trustedsiteszoneallowuserdatapersistence)
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb9d2-839">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="eb9d2-839">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="eb9d2-840">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="eb9d2-840">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="eb9d2-841">TrustedSitesZoneDoNotRunAntimalwareAgainstActiveXControls</span><span class="sxs-lookup"><span data-stu-id="eb9d2-841">TrustedSitesZoneDoNotRunAntimalwareAgainstActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-trustedsiteszonedonotrunantimalwareagainstactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb9d2-842">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="eb9d2-842">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="eb9d2-843">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="eb9d2-843">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="eb9d2-844">TrustedSitesZoneDontRunAntimalwareProgramsAgainstActiveXControls</span><span class="sxs-lookup"><span data-stu-id="eb9d2-844">TrustedSitesZoneDontRunAntimalwareProgramsAgainstActiveXControls</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb9d2-845">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="eb9d2-845">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="eb9d2-846">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="eb9d2-846">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="eb9d2-847">TrustedSitesZoneInitializeAndScriptActiveXControls</span><span class="sxs-lookup"><span data-stu-id="eb9d2-847">TrustedSitesZoneInitializeAndScriptActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-trustedsiteszoneinitializeandscriptactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb9d2-848">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="eb9d2-848">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="eb9d2-849">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="eb9d2-849">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="eb9d2-850">TrustedSitesZoneInitializeAndScriptActiveXControlsNotMarkedAsSafe</span><span class="sxs-lookup"><span data-stu-id="eb9d2-850">TrustedSitesZoneInitializeAndScriptActiveXControlsNotMarkedAsSafe</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb9d2-851">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="eb9d2-851">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="eb9d2-852">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="eb9d2-852">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="eb9d2-853">TrustedSitesZoneInitializeAndScriptActiveXControlsNotMarkedSafe</span><span class="sxs-lookup"><span data-stu-id="eb9d2-853">TrustedSitesZoneInitializeAndScriptActiveXControlsNotMarkedSafe</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb9d2-854">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="eb9d2-854">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="eb9d2-855">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="eb9d2-855">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="eb9d2-856">TrustedSitesZoneJavaPermissions</span><span class="sxs-lookup"><span data-stu-id="eb9d2-856">TrustedSitesZoneJavaPermissions</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-trustedsiteszonejavapermissions)
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb9d2-857">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="eb9d2-857">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="eb9d2-858">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="eb9d2-858">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="eb9d2-859">TrustedSitesZoneNavigateWindowsAndFrames</span><span class="sxs-lookup"><span data-stu-id="eb9d2-859">TrustedSitesZoneNavigateWindowsAndFrames</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-trustedsiteszonenavigatewindowsandframes)
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb9d2-860">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="eb9d2-860">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="eb9d2-861">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="eb9d2-861">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="eb9d2-862">Requisitos</span><span class="sxs-lookup"><span data-stu-id="eb9d2-862">Requirements</span></span>



| <span data-ttu-id="eb9d2-863">Requisito</span><span class="sxs-lookup"><span data-stu-id="eb9d2-863">Requirement</span></span> | <span data-ttu-id="eb9d2-864">Value</span><span class="sxs-lookup"><span data-stu-id="eb9d2-864">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="eb9d2-865">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="eb9d2-865">Minimum supported client</span></span><br/> | <span data-ttu-id="eb9d2-866">Solo aplicaciones de escritorio de Windows 10 \[\]</span><span class="sxs-lookup"><span data-stu-id="eb9d2-866">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="eb9d2-867">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="eb9d2-867">Minimum supported server</span></span><br/> | <span data-ttu-id="eb9d2-868">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="eb9d2-868">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="eb9d2-869">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="eb9d2-869">Namespace</span></span><br/>                | <span data-ttu-id="eb9d2-870">Dmmap de MDM raíz de \\ cimv2 \\ \\</span><span class="sxs-lookup"><span data-stu-id="eb9d2-870">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="eb9d2-871">MOF</span><span class="sxs-lookup"><span data-stu-id="eb9d2-871">MOF</span></span><br/>                      | <dl> <span data-ttu-id="eb9d2-872"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="eb9d2-872"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="eb9d2-873">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="eb9d2-873">DLL</span></span><br/>                      | <dl> <span data-ttu-id="eb9d2-874"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="eb9d2-874"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



 

